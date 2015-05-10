---
title: Slave
layout: page
permalink: mysql/slave/
---

# How to setup a mysql slave
See [http://www.percona.com/doc/percona-xtrabackup/2.1/howtos/setting_up_replication.html]

= Start

```mysql
START SLAVE;
```

# Stop

```mysql
STOP SLAVE;
```

# Status

```mysql
SHOW SLAVE STATUS \G;
```

# Make slave jump current instruction

```mysql
STOP SLAVE;
SET GLOBAL sql_slave_skip_counter = 1;
START SLAVE;
```
