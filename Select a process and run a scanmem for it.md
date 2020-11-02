```bash 
$ ps -aux | fzf | awk '{print $2}' | xargs -o scanmem -p
```

It will display a list of processes with *fuzzy find* ([fzf](https://github.com/junegunn/fzf)) and run `scanmem` for the selected one. [Scanmem](https://github.com/scanmem/scanmem) is a process memory editing tool that does the same stuff as [ArtMoney](http://artmoney.ru/eng.htm) does for [/Windows]().