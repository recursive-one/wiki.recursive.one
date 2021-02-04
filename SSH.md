# SSH Agent Forwarding

One may want to use the local keys from the remote machine to do `git push` for example. This goal is achievable by copying of keys to the remote machine. But also one can use the "SSH Agent Forwarding" and keep all the keys safely an locally.

Agent forwarding is a built-in feature. All you need is to enable it for some/all hosts using `ssh_config`:

```
Host foo
    ForwardAgent yes
```