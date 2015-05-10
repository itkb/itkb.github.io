---
title: yum
layout: page
permalink: linux/cli/commands/yum/
---

YUM is the default dependency manager for RedHat based distributions.

# Install a package
To install a package the following command is used:

```bash
yum install PACKAGENAME
```

# Search a package
There are several ways to search a package based on the information you have. If you know part of the package name, you can use

```bash
yum search STRING
```

If you know the command or file you want to use but don't know the package name, you can use

```bash
yum provides */FILE
```

For example, if you want to install zcat but don't know the package name that provide it, you can use

```bash
yum provides */zcat
```

# Update packages
To update all packages that have been installed with yum to the latest version provided by your Linux Vendor, use

```bash
yum update
```

# Check installed software information
To check if you have a specific package installed, you can use:

```bash
yum list installed | grep PACKAGE
```

This provides also the current installed version and the repository from which the package comes from.
