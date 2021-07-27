---
categories: Linux
...

# Ubuntu/Debian

See [/Packaging in Debian]()

## Tweaks

### Keyboard & layouts

My preferences:

- `Caps` as `Ctrl`
- `LCtrl` enables English layout
- `RCtrl` enables Russian layout
- `RAlt` switches to other layout *when pressed*
- `PrtSc` works as the [Compose key](https://en.wikipedia.org/wiki/Compose_key)

How to

1.

    ```ini
    # /etc/default/keyboard
    XKBMODEL="pc105"
    XKBLAYOUT="us,ru"
    XKBVARIANT=","
    XKBOPTIONS="compose:prsc,ctrl:nocaps,grp:lctrl_rctrl_switch,grp:switch"
    ```

2.

    ```bash
    sudo dpkg-reconfigure keyboard-configuration
    ```

### Discrete GPU

```bash
$ glxinfo | grep "OpenGL renderer"
OpenGL renderer string: Mesa DRI Intel(R) HD Graphics ...
$ # hmm
$ DRI_PRIME=1 glxinfo | grep OpenGL renderer
OpenGL renderer string: AMD HAINAN ...
$ # a-ha!
$ DRI_PRIME=1 ./game
```