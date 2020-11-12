Pinentry is not supposed to be used from Bash due to its protocol, but if you realy want:

```bash
{ echo "SETDESC KeePassXC"; echo "SETPROMPT PASS:"; echo "GETPIN"; } | pinentry-curses  -T $TTY -C UTF-8 | sed -n 's
/^D //p' | whatever-you-want
```