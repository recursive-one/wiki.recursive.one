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

### Customizing `xdg-open`

Example of .desktop file (put in `~/.local/share/applications`):

```ini
[Desktop Entry]
Version=1.0
Name=GNU Emacs (GUI)
GenericName=Text Editor
Comment=GNU Emacs is an extensible, customizable text editor - and more
MimeType=text/english;text/plain;text/x-makefile;text/x-c++hdr;text/x-c++src;text/x-chdr;text/x-csrc;text/x-java;text/x-moc;text/x-pascal;text/x-tcl;text/x-tex;application/x-shellscript;text/x-c;text/x-c++;
Exec=/usr/bin/emacsclient -c %F
Icon=emacs25
Type=Application
Terminal=false
Categories=Utility;Development;TextEditor;
StartupWMClass=Emacs
Keywords=Text;Editor;
```

How to get the type:

```shell
$ mimetype foo.jpg
```

How to associate app (its .desktop file) with type:

```shell
$ xdg-mime default imv.desktop image/jpeg
```

([source](https://200ok.ch/posts/2022-01-12_configuring_default_applications_for_xdg_open.html))