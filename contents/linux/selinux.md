---
title: SELinux
layout: page
permalink: linux/selinux/
---

# Status, start and stop
Get selinux status

```bash
getenforce
```

Enable selinux

```bash
setenforce true
```

Disable selinux

```bash
setenforce false
```

# Reset permissions
Restore permissions of files in a folder

```bash
restorecon -Rv FOLDER
```
