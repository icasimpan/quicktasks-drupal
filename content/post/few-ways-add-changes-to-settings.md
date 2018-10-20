---
title: "Few Ways to Add Changes to settings.php"
date: 2018-04-09T00:20:33+08:00
draft: false
---

*Method 1 (env.json)*
in drupalroot/sites/default/env.json

```
{
  "conf_dir": "/etc/drupal/site_identifier_here/default"
}

```

in /etc/drupal/site_identifier_here/default, there is then a file _globals.conf.d/globals.default.json_ with content:

```
{
  "id": "default",
  "databases": {
    "default": {
      "default": {
        "database": "yourDB",
        "username": "yourDBA",
        "password": "yourPASS",
        "host": "127.0.0.1",
        "driver": "mysql"
      }
    }
  },
  "uri": "example.com",
  "doc_root": "www",
  "chef_type": "data_bag_item",
  "data_bag": "drupal"
}

*Method 2: Referenced from settings.php*

In drupalroot/sites/default/settings.php, there is this code snippet:

```
 if (file_exists($app_root . '/' . $site_path . '/settings.local.php')) {
   include $app_root . '/' . $site_path . '/settings.local.php';
 }
```

Then, said referred file's content as follows:
```
<?php
$databases['default']['default'] = array (
  'database' => 'yourDB',
  'username' => 'yourDBA',
  'password' => 'yourPASS',
  'prefix' => '',
  'host' => 'localhost',
  'port' => '3306',
  'namespace' => 'Drupal\\Core\\Database\\Driver\\mysql',
  'driver' => 'mysql',
);
?>
```

