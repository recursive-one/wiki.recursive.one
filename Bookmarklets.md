"Bookmarklet" = "bookmark" + "applet", is a chunk of JavaScript that you save as a bookmark for your browser. When you click on a bookmarklet its script runs in the context of the current page and applies some magic to it.

Here you can found some bookmarklets we found on the Web. You can just copy-paste them into the address field during bookmark creation!

## UX fixes

### "readable"

Found [here](https://www.arp242.net/bookmarklets.html). Makes pages more readable.

```
javascript:(function() {
    document.querySelectorAll('p, li, div').forEach(function(n) {
        n.style.color = '#000';
        n.style.font = '500 16px/1.7em sans-serif';
    });
})();
```

### "fixed"

Found [here](https://www.arp242.net/bookmarklets.html). Unpins some "pinned" toolbars fixed again (makes them scrollable as other content)!

```
javascript:(function() {
    document.querySelectorAll('*').forEach(function(n) {
        var p = getComputedStyle(n).getPropertyValue('position');
        if (p === 'fixed' || p === 'sticky') {
            n.style.cssText += ' ; position: absolute !important;';
        }
    });
})();
```

## Crazy stuff

### awfice

[awfice](https://zserge.com/posts/awfice/), the "World smallest office suite" - a collection of "apps" each of those fits inside the bookmark. Total fun!

The simplest one - a *Rich Text Editor* (Ctrl+B, Ctrl+I, that stuff):

```
data:text/html,<body contenteditable style=line-height:1.5;font-size:20px>
```
