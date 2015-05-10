---
title: Crontab
layout: page
permalink: linux/crontab/
---

The crontab is a utility for Job Scheduling.

To see the current running crontab, use `crontab -l`, while to edit it, `crontab -e`.

# Syntax
Every line in the crontab have to follow this schema:

```bash
 # ┌───────────────────────── min (0 - 59)
 # │    ┌──────────────────── hour (0 - 23)
 # │    │    ┌─────────────── day of month (1 - 31)
 # │    │    │    ┌────────── month (1 - 12)
 # │    │    │    │    ┌───── day of week (0 - 7) (0 to 6 are Sunday to Saturday; 7 is Sunday agian)
 # │    │    │    │    │
 # │    │    │    │    │
   *    *    *    *    *      USER    COMMAND
```

All the first 5 parameters can be used in different modes:

```crontab
* * means ALL (ie: * * * * * means every minute 24/7/365)
* */N means every N (ie: */5 in the first column means every 5 minutes)
```
