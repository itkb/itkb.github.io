---
title: awk
layout: page
permalink: linux/cli/commands/awk/
---

# Group by
-F modificatore di colonna
$1 colonna da grouppare

```bash
awk -F";" 'NR>1{arr[$1]++}END{for (a in arr) print a, arr[a]}'
```

# Print all lines with N columns

```bash
awk 'NF==2{print}{}'
```

# Examples

Show date:

```bash
awk -v date="$(date +"%d-%m-%Y %H:%M:%S")" '{print date}'
```
