---
title: Bash Shell
layout: page
permalink: linux/bash-shell/
---

GNU Bash is one most used shell in Linux and is the default shell for many distributions like Fedora, Red Hat, CentOS.

## Keystrokes
* *CTRL + A:* Bring the cursot at the begin of the current command line
* *CTRL + B:* Brign the cursor at the end of the current command line
* *CTRL + C:* Quit the current executed command or task
* *CTRL + D:* Send an End Of File (EOF) signal
* *CTRL + R:* Reverse search for commands history
* *CTRL + Z:* Stop the current executed command or task (to resume, use fg or bg)

## Hisotry
Every command you type in bash is saved in the bash history that is kept in the file `~/.bash_history`.

To clean the history you can:

* Delete the `~/.bash_history` file (you must be *`root`* to perform this action)
* Run `history -c` to tell bash to clean it for you

NOTE: All commands are stored in bash history, so is better not to put passwords as inline parameters to any command.

