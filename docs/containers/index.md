# Containers 

## Overview

The WordPress stack consist of the following containers:

| Container    | Versions           | Image                              |
| ------------ | ------------------ | ---------------------------------- |
| [Nginx]      | 1.13, 1.12         | [wodby/wordpress-nginx]            |
| [Apache]     | 2.4                | [wodby/php-apache]                 |
| [PHP]        | 7.1, 7.0, 5.6      | [wodby/wordpress-php]              |
| [MariaDB]    | 10.2, 10.1         | [wodby/mariadb]                    |
| [PostgreSQL] | 10.1, 9.6          | [wodby/postgres]                   |
| [Redis]      | 4.0, 3.2           | [wodby/redis]                      |
| [Varnish]    | 4.1                | [wodby/wordpress-varnish]          |
| [OpenSMTPD]  | 6.0                | [wodby/opensmtpd]                  |
| [Webgrind]   | 1.5                | [wodby/webgrind]                   |
| [Blackfire]  | latest             | [blackfire/blackfire]              |
| [Rsyslog]    | latest             | [wodby/rsyslog]                    |
| [AthenaPDF]  | 2.10.0             | [arachnysdocker/athenapdf-service] |
| Mailhog      | latest             | [mailhog/mailhog]                  |
| Adminer      | 4.3                | [wodby/adminer]                    |
| phpMyAdmin   | latest             | [phpmyadmin/phpmyadmin]            |

!!! note "SSHD and Cron":
    For Wodby environments we additionally spin up copies of PHP services with overridden commands to run cron and ssh daemons. All environment variables added to PHP service will be automatically passed to [SSHD] and [Cron] services.

## Configuration

Every container provides a set of environment variables for its customization. You can add and edit environment variables of a service from `[Instance] > Stack` page. For more details see https://docs.wodby.com/stacks/configuration.html  

[Apache]: apache.md
[AthenaPDF]: athenapdf.md
[Blackfire]: blackfire.md
[Mailhog]: mailhog.md
[MariaDB]: mariadb.md
[Nginx]: nginx.md
[OpenSMTPD]: opensmtpd.md
[PHP]: php.md
[PostgreSQL]: postgres.md
[Redis]: redis.md
[Rsyslog]: rsyslog.md
[Varnish]: varnish.md
[Webgrind]: webgrind.md

[SSHD]: ssh.md
[Cron]: cron.md

[wodby/wordpress-nginx]: https://github.com/wodby/wordpress-nginx
[wodby/php-apache]: https://github.com/wodby/php-apache
[wodby/wordpress]: https://github.com/wodby/wordpress
[wodby/wordpress-php]: https://github.com/wodby/wordpress-php
[wodby/mariadb]: https://github.com/wodby/mariadb
[wodby/postgres]: https://github.com/wodby/postgres
[wodby/redis]: https://github.com/wodby/redis
[wodby/opensmtpd]: https://github.com/wodby/opensmtpd
[wodby/wordpress-varnish]: https://github.com/wodby/wordpress-varnish
[wodby/memcached]: https://github.com/wodby/memcached
[wodby/webgrind]: https://hub.docker.com/r/wodby/webgrind
[blackfire/blackfire]: https://hub.docker.com/r/blackfire/blackfire
[wodby/rsyslog]: https://hub.docker.com/r/wodby/rsyslog
[arachnysdocker/athenapdf-service]: https://hub.docker.com/r/arachnysdocker/athenapdf-service
[mailhog/mailhog]: https://hub.docker.com/r/mailhog/mailhog
[wodby/adminer]: https://hub.docker.com/r/wodby/adminer
[phpmyadmin/phpmyadmin]: https://hub.docker.com/r/phpmyadmin/phpmyadmin
[portainer/portainer]: https://hub.docker.com/portainer/portainer
[_/node]: https://hub.docker.com/_/node
[_/traefik]: https://hub.docker.com/_/traefik
