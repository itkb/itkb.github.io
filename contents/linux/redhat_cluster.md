---
title: Red Hat Cluster
layout: page
permalink: linux/redhat-cluster/
---

# Deploy new version

First of all let's check if the edit is ok:

```bash
ccs_config_validate -f /root/cluster.conf
```

Then copy it to the right location

```bash
cp /root/cluster.conf /etc/cluster/cluster.conf
```

Then propagate

```bash
cman_tool version -r
```

# Check if the new version has been propagated properly

To check the current version of the cluster on a specific machine, run:

```bash
head -2 /etc/cluster/cluster.conf | tail -1 | sed -r 's/.*"([0-9]+)".*/\1/'
```
