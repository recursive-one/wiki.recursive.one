[Zenity](https://help.gnome.org/users/zenity/) is a GTK+ powered alternative for the [dialog(1)](https://linux.die.net/man/1/dialog) and the [whiptail(1)](https://linux.die.net/man/1/whiptail).

It can display

- text or password entry
- calendar (date selector)
- file/directory selector
- color chooser
- confirmation
- "info"
- "warning"
- ...

User input Zenity dumps to STDOUT so you can easily integrate any dialog into your shell scripts.

Also, Zenity can show the desktop notifications and the progress indicators.

# Examples
- OS Suspend confirmation:

    ```bash
    if zenity --question --text="Suspend?" --default-cancel; then
        systemctl suspend
    fi
    ```

- A shopping list (from `man zenity`):

    ```bash
    zenity --list --checklist --column "Buy" --column "Item" \
        TRUE Apples \
        TRUE Oranges \
        FALSE Pears \
        FALSE Toothpaste
    ```

- A notification (from `man zenity`):

    ```bash
    zenity --notification --window-icon=update.png --text "System update necessary!"
    ```

# Wrappers

There are many wrappers for the different programming languages. Here is a couple of them:

- [hzenity](https://hackage.haskell.org/package/hzenity) for [/Haskell]()
- [zenipy](https://github.com/poulp/zenipy) for [/Python]()