# WordPress settings

## wp-config.php

Wodby automatically adds include of `wodby.wp-config.php` to `wp-config.php` file in WP root. If the file does not exist Wodby will create it automatically.

Do not edit `wodby.wp-config.php`, all changes to this file will be reset.

The `wodby.wp-config.php` file contains configuration settings for integration with Wodby services such as Database, Cache storage and Reverse Caching Proxy. You can override settings specified in `wodby.wp-config.php` in your `wp-config.php` file after the include.

## Files

Files for WordPress located in `/mnt/files/public` and symlinked to `wp-content/uploads`.

## Base URL

The domain marked with primary flag will be used as a `WP_HOME` and `WP_SITEURL` in `wodby.wp-config.php` file.
