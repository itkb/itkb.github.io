---
title: Users
layout: page
permalink: mysql/users/
---

# User creation

Create the user [USER] with password [PASSWORD] reachable from [IP_RANGE] with replication permissions:

```mysql
GRANT REPLICATION SLAVE ON *.*  TO '[USER]'@'[IP_RANGE]' IDENTIFIED BY '[PASSWORD]';
```

Create the user [USER] with password [PASSWORD] reachable from [IP_RANGE] with root permissions:

```mysql
GRANT ALL ON *.*  TO '[USER]'@'[IP_RANGE]' IDENTIFIED BY '[PASSWORD]';
```

# Change password

```mysql
SET PASSWORD FOR '[USER]'@'[IP_RANGE]' = PASSWORD('[PASSWORD]');
```
