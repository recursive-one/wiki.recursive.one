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

How to

1.

    ```ini
    # /etc/default/keyboard
    XKBMODEL="pc105"
    XKBLAYOUT="us,ru"
    XKBVARIANT=","
    XKBOPTIONS="ctrl:nocaps,grp:lctrl_rctrl_switch,grp:switch"
    ```

2.

    ```bash
    sudo dpkg-reconfigure keyboard-configuration
    ```