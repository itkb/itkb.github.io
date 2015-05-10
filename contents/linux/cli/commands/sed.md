---
title: sed
layout: page
permalink: linux/cli/commands/sed/
---

GNU Sed is a powerful tool for string manipulation

# Basic syntax
The most basic example of `sed` is:

```bash
echo 'a' | sed 's/a/b/'
```

Even if the first part of command will echo "a", the whole command will echo "b", since sed will substitute every instance of "a" with the string "b".
