# Backups

This stack provides backup and restore actions for files (e.g. `wp-content/uploads`) and database. Learn more about backups from our [documentation](https://help.wodby.com/apps/backups).

## Database backups

MariaDB backups run with [--single-transaction](https://dev.mysql.com/doc/refman/5.7/en/mysqldump.html) option to avoid tables locks.
