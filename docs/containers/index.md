# Containers 

## Overview

The WordPress stack consist of the following containers:

| Container    | Versions           | [Resources]      | Image                              |
| ------------ | ------------------ | ---------------- | ---------------------------------- |
| [Apache]     | 2.4                | 4m               | [wodby/php-apache]                 |
| [AthenaPDF]  | 2.10.0             | 16m              | [arachnysdocker/athenapdf-service] |
| [Blackfire]  | latest             | 4m               | [blackfire/blackfire]              |
| [Crond]      | -                  | 4m, 0.1; 512m, 1 | [wodby/wordpress-php]              |
| [Mailhog]    | latest             | 4m               | [mailhog/mailhog]                  |
| [MariaDB]    | 10.3, 10.2, 10.1   | 128m             | [wodby/mariadb]                    |
| [Memcached]  | 1.5                |                  | [wodby/memcached]                  |
| [Nginx]      | 1.15, 1.14, 1.13   | 4m               | [wodby/wordpress-nginx]            |
| [Node.js]    | 9.11, 8.11, 6.14   |                  | [wodby/node]                       |
| [OpenSMTPD]  | 6.0                | 4m               | [wodby/opensmtpd]                  |
| [PHP]        | 7.x, 5.6           | 32m              | [wodby/wordpress-php]              |
| [PostgreSQL] | 10, 9.x            | 64m              | [wodby/postgres]                   |
| [Redis]      | 4.0, 3.2           | 4m               | [wodby/redis]                      |
| [Rsyslog]    | latest             | 4m               | [wodby/rsyslog]                    |
| [SSHD]       | -                  | 4m               | [wodby/wordpress-php]              |
| [Varnish]    | 4.1                | 8m               | [wodby/wordpress-varnish]          |
| [Webgrind]   | 1.5                | 16m              | [wodby/webgrind]                   |
| Adminer      | 4.3                | 8m               | [wodby/adminer]                    |
| Mailhog      | latest             | 4m               | [mailhog/mailhog]                  |
| phpMyAdmin   | latest             | 32m              | [phpmyadmin/phpmyadmin]            |

!!! note "Resources"
    Default values specified. `4m, 0.1; 512m, 1` means 4m RAM and 0.1 CPU requests; 512m RAM and 1 CPU limits. For more details visit https://help.wodby.com/stacks/configuration#resources

!!! note "SSHD and Cron"
    For Wodby environments we additionally spin up copies of PHP services with overridden commands to run cron and ssh daemons. All environment variables added to PHP service will be automatically passed to [SSHD] and [Crond] services.

## Configuration

Every container provides a set of environment variables for its customization. You can add and edit environment variables of a service from `[Instance] > Stack` page. For more details see https://help.wodby.com/stacks/configuration  

[Apache]: apache.md
[AthenaPDF]: athenapdf.md
[Blackfire]: blackfire.md
[Crond]: cron.md
[Mailhog]: mailhog.md
[MariaDB]: mariadb.md
[Memcached]: memcached.md
[Nginx]: nginx.md
[Node.js]: node.md
[OpenSMTPD]: opensmtpd.md
[PHP]: php.md
[PostgreSQL]: postgres.md
[Redis]: redis.md
[Rsyslog]: rsyslog.md
[SSHD]: ssh.md
[Varnish]: varnish.md
[Webgrind]: webgrind.md

[_/node]: https://hub.docker.com/_/node
[_/traefik]: https://hub.docker.com/_/traefik
[arachnysdocker/athenapdf-service]: https://hub.docker.com/r/arachnysdocker/athenapdf-service
[blackfire/blackfire]: https://hub.docker.com/r/blackfire/blackfire
[mailhog/mailhog]: https://hub.docker.com/r/mailhog/mailhog
[phpmyadmin/phpmyadmin]: https://hub.docker.com/r/phpmyadmin/phpmyadmin
[portainer/portainer]: https://hub.docker.com/portainer/portainer
[wodby/adminer]: https://hub.docker.com/r/wodby/adminer
[wodby/mariadb]: https://github.com/wodby/mariadb
[wodby/memcached]: https://github.com/wodby/memcached
[wodby/opensmtpd]: https://github.com/wodby/opensmtpd
[wodby/php-apache]: https://github.com/wodby/php-apache
[wodby/postgres]: https://github.com/wodby/postgres
[wodby/redis]: https://github.com/wodby/redis
[wodby/rsyslog]: https://hub.docker.com/r/wodby/rsyslog
[wodby/webgrind]: https://hub.docker.com/r/wodby/webgrind
[wodby/wordpress-nginx]: https://github.com/wodby/wordpress-nginx
[wodby/wordpress-php]: https://github.com/wodby/wordpress-php
[wodby/wordpress-varnish]: https://github.com/wodby/wordpress-varnish
[wodby/wordpress]: https://github.com/wodby/wordpress
