---
categories: Linux bash
toc: no
title: Which Linux is this
...

Right now I'm trying to wrap my head around the script that gives a robust way to get the Linux distribution name and its version. 

First option is to parse `/etc/os-release` file for `ID` and `VERSION_ID`. The problem is that, for example, Centos6 has no such file, but has his own `/etc/centos-release` and `/etc/redhat-release` files. 

The second option is to handle `lsb_release` command output. The problem in this case that the command is not available by default and should be satisfied by installing additional packages. 

In the end, I have to combine all the above methods and fallback from one to another if something went wrong.