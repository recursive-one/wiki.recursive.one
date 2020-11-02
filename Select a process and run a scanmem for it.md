```bash 
$ ps -aux | fzf | awk '{print $2}' | xargs -o scanmem -p
```

It will display a list of processes with fuzzy find (fzf) and run `scanmem` for the selected one. Scanmem is a process memory editing tool that does the stuff as ArtMoney does for Windows.