---
format: md
categories: linux bash
toc: no
title: Which linux is this
...

Right now I'm trying to wrap my head around the script that gives a robust way to get the linux distribution name and its version. 

First option is to parse `/etc/os-release` file for `ID` and `VERSION_ID`. The problem is that, for example Centos6 has no such file.

The second option is to handle `lsb_release` command output. The problem in this case that the command is not available by default and should be satisfyed by installing additional packages. 

In the end, I have to combine all above methods and fallback from one to another if somethings gone wrong.