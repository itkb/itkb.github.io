---
title: Mysqldump
layout: page
permalink: mysql/mysqldump/
---

Mysql dump is used to dump mysql databases to files

Dump all databases (mysql included):

```bash
mysqldump -u[MYSQL_USER] -u[MYSQL_PASS] --all-databases | gzip > [PATH].gz
```

Dump only selected databases:

```bash
mysqldump -u[MYSQL_USER] -u[MYSQL_PASS] --databases [DATABASE_LIST_SPACE_SEPARATED] | gzip > [PATH].gz
```

Dump all dbs creation statements and triggers, without data:

```bash
mysqldump -u[MYSQL_USER] -u[MYSQL_PASS] --no-data --no-create-info --all-databases --routines > [PATH]
```

Dump all create statements (dbs, tables, views) without data and triggers:

```bash
mysqldump -u[MYSQL_USER] -p[MYSQL_PASSWORD] --no-data --all-databases > [PATH]
```

Sometimes is necessary to ignore tables or views. This is possible using the `--ignore-table=[DB].[TABLE]` statement.
