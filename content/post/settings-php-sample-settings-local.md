---
title: "settings.php: Sample settings.local.php"
date: 2018-04-09T00:20:25+08:00
draft: false
---

```
<?php
$databases['default']['default'] = array (
  'database' => 'yourDB',
  'username' => 'yourDBA',
  'password' => 'yourDBPASS',
  'prefix' => '',
  'host' => 'localhost',
  'port' => '3306',
  'namespace' => 'Drupal\\Core\\Database\\Driver\\mysql',
  'driver' => 'mysql',
);
?>
```
