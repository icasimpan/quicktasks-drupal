---
title: "Drupal maintenance mode (turn-off) via drush"
date: 2018-04-09T00:20:25+08:00
draft: false
---

# Drupal 8
```
drush sset system.maintenance_mode FALSE
```

# Drupal 7
```
drush vset maintenance_mode 0
```
You may need to clear cache for it to work.
