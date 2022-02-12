# SOCKS5 proxy over SSH

```shell
ssh -D 9000 -qNC [-f] user@host
```

where

- `-D port` open a SOCKS proxy locally
- `-q` be quiet
- `-N` no command execution
- `-C` use compression
- `-f` run in the background