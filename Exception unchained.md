---
categories: Python
toc: no
...

# Exception **unchained**

There is the [PEP-3134](https://www.python.org/dev/peps/pep-3134/). TLDR: it's all about `raise ... from`.

This method I am finding pretty useful when I have to build an abstraction barrier:

```python
class ProcessingError(Exception):
    pass

def process(data):
    try:
        use(data['baz'][42]['qux']['doo'])
    except (KeyError, IndexError) as e:
        raise ProcessingError('Data has a bad shape') from e
```

Here I have some "*low-level*" (or "*internal*") errors (`KeyError`, `IndexError`) and the "*hi-level*" (or "*public*") one — `ProcessingError`. This high-level error abstracts the implementation and delivers a way more descriptive message. But if I'll need to do some investigation I definitely will need an actual error. That's why I am using `raise ... from`. Now I can get access to the original exception in the `__cause__` attribute of the hi-level one.

But here I have one "but" (`:)`): I can't format such chained errors as I can do with the recently raised one. The `traceback` module provides many blows and whistles. And the `logging` also can store formatted errors. But all this stuff is tightly coupled with the "exception info" — a type of triples (i.e. `tuple`) with *exception class*, *exception value*, and *traceback object* inside. Such triples you usually can get by calling of `sys.exc_info()`, but this function always returns the most recent exception — yep(!), the `ProcessingError`!

Here is a workaround I use:

```python
try:
    process({})
except ProcessingError as e:
    cause = e.__cause__
    cause_info = (cause.__class__, cause, cause.__traceback__)
    # yep, an original error has it's own traceback --^
    logging.debug(str(e), exc_info=cause_info)
    logging.error(str(e))  # A high-level (user-friendly) error
```


## An easy way

If you don't need to strip out the high-level layer, you can just do `logging.debug(str(e), exc_info=sys.exc_info())` or even `logging.debug(str(e), exc_info=True)`. Then you will just get both errors in a row:

```text
Traceback (most recent call last):
...
KeyError: ...

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
...
ProcessingError: ...
```

Yes, just it! I definitely think what this is the main reason why all the `exc_info` stuff so cumbersome: you should use (and want to use) such easy ways.