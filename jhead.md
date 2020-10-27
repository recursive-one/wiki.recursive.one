---
toc: no
categories: Linux
...

# jhead

[jhead(1)](https://www.sentex.net/~mwandel/jhead/), the "[Exif](https://en.wikipedia.org/wiki/Exif) Jpeg header manipulation tool". This thing is pretty useful when you need to take some Exif data from your photos and use it to rename those files for example.

## How to get

Just as usual:

```shell
$ sudo apt-get install jhead
```

## Some ways I use it

-   Rename files using its timestamps:

    ```shell
    $ jhead -n%Y%m%d_%H%M%S *.jpg
    ```

-   Tweak the timestamps itself (if you forgot to set up the timezone for your camera):

    ```shell
    $ jhead -ta+5:00 *.jpg
    ```