---
title: rpm
layout: page
permalink: linux/cli/commands/rpm/
---

RPM is the default package manager software for Red Hat based distributions.

# Install a package
To install a package from rpm, run:

```bash
rpm -ivh RPMFILE
```

# Find information about an installed package
To find the *version of an installed package*, simply run:

```bash
rpm -qa PACKAGENAME
```

To find all *files in a package*, run

```bash
rpm -ql PACKAGENAME
```

To find all *documentation in a package*, run

```bash
rpm -qd PACKAGENAME
```
