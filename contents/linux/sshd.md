---
title: SSHd
layout: page
permalink: linux/sshd/
---

# Check config file
To be sure that that issued config file is correct, please run

```bash
/usr/bin/sshd -T
```

# Speed up login

```bash
GSSAPIAuthentication yes -> GSSAPIAuthentication no
```
