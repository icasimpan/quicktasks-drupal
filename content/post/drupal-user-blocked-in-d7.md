---
title: "Drupal User Blocked in D7"
date: 2020-06-16T00:20:25+08:00
tags: [drupal, user, blocked, reset]
draft: false
---

How to reset user after being blocked (d7 only)?

```
MySQL> delete from flood where identifier=<uid>;
```

To get the uid, search as follows:
```
MySQL> select uid, name from users where name like '%NameHere%'\G;
```

Details in https://www.drupal.org/node/1023440
