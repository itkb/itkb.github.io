---
title: Mysqlbinlog
layout: page
permalink: mysql/mysqlbinlog/
---

Mysql binlog is used to dump binlogs to "readable" files

```bash
mysqlbinlog --verbose --base64-output=decode-rows mysql-bin.000XXX > mysql-bin.000XXX-decoded
```
