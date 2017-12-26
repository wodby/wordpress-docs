# Local environment with Docker4WordPress

Docker4WordPress is an open-source project ([GitHub page](https://github.com/wodby/docker4wordpress)) that provides pre-configured `docker-compose.yml` file from to spin up local environment on Linux, Mac OS X and Windows. 

## Requirements

* [Install Docker Compose](https://docs.docker.com/compose/install)

The WordPress stack consist of the following containers:

| Container    | Versions           | Service name | Image                              |
| ------------ | ------------------ | ------------ | ---------------------------------- |
| [Nginx]      | 1.13, 1.12         | `nginx`      | [wodby/wordpress-nginx]            |
| [Apache]     | 2.4                | `apache`     | [wodby/php-apache]                 |
| WordPress    | 4                  | `php`        | [wodby/wordpress]                  |
| [PHP]        | 7.x, 5.6           | `php`        | [wodby/wordpress-php]              |
| [MariaDB]    | 10.2, 10.1         | `mariadb`    | [wodby/mariadb]                    |
| [PostgreSQL] | 10.1, 9.6          | `postgres`   | [wodby/postgres]                   |
| [Redis]      | 4.0, 3.2           | `redis`      | [wodby/redis]                      |
| [Varnish]    | 4.1                | `varnish`    | [wodby/wordpress-varnish]          |
| [Webgrind]   | 1.5                | `webgrind`   | [wodby/webgrind]                   |
| [Blackfire]  | latest             | `blackfire`  | [blackfire/blackfire]              |
| [AthenaPDF]  | 2.10.0             | `athenapdf`  | [arachnysdocker/athenapdf-service] |
| Mailhog      | latest             | `mailhog`    | [mailhog/mailhog]                  |
| phpMyAdmin   | latest             | `pma`        | [phpmyadmin/phpmyadmin]            |
| Portainer    | latest             | `portainer`  | [portainer/portainer]              |
| Traefik      | latest             | `traefik`    | [_/traefik]                        |

[Apache]: ../containers/apache.md
[AthenaPDF]: ../containers/athenapdf.md
[Blackfire]: ../containers/blackfire.md
[Mailhog]: ../containers/mailhog.md
[MariaDB]: ../containers/mariadb.md
[Memcached]: ../containers/memcached.md
[Nginx]: ../containers/nginx.md
[Node.js]: ../containers/nodejs.md
[OpenSMTPD]: ../containers/opensmtpd.md
[PHP]: ../containers/php.md
[PostgreSQL]: ../containers/postgres.md
[Redis]: ../containers/redis.md
[Rsyslog]: ../containers/rsyslog.md
[Solr]: ../containers/solr.md
[Varnish]: ../containers/varnish.md
[Webgrind]: ../containers/webgrind.md

[wodby/wordpress-nginx]: https://github.com/wodby/wordpress-nginx
[wodby/php-apache]: https://github.com/wodby/php-apache
[wodby/wordpress]: https://github.com/wodby/wordpress
[wodby/wordpress-php]: https://github.com/wodby/wordpress-php
[wodby/mariadb]: https://github.com/wodby/mariadb
[wodby/postgres]: https://github.com/wodby/postgres
[wodby/redis]: https://github.com/wodby/redis
[wodby/wordpress-varnish]: https://github.com/wodby/wordpress-varnish
[wodby/webgrind]: https://hub.docker.com/r/wodby/webgrind
[blackfire/blackfire]: https://hub.docker.com/r/blackfire/blackfire
[arachnysdocker/athenapdf-service]: https://hub.docker.com/r/arachnysdocker/athenapdf-service
[mailhog/mailhog]: https://hub.docker.com/r/mailhog/mailhog
[phpmyadmin/phpmyadmin]: https://hub.docker.com/r/phpmyadmin/phpmyadmin
[portainer/portainer]: https://hub.docker.com/portainer/portainer
[_/traefik]: https://hub.docker.com/_/traefik
