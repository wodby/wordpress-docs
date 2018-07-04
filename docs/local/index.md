# Local environment with Docker4WordPress

Docker4WordPress is an open-source project ([GitHub page](https://github.com/wodby/docker4wordpress)) that provides pre-configured `docker-compose.yml` file from to spin up local environment on Linux, Mac OS X and Windows. 

## Requirements

* [Install Docker Compose](https://docs.docker.com/compose/install)

The WordPress stack consist of the following containers:

| Container     | Versions           | Service name    | Image                              |
| ------------- | ------------------ | --------------- | ---------------------------------- |
| [Nginx]       | 1.15, 1.14, 1.13   | `nginx`         | [wodby/wordpress-nginx]            |
| [Apache]      | 2.4                | `apache`        | [wodby/php-apache]                 |
| [PHP]         | 7.x, 5.6           | `php`           | [wodby/wordpress-php]              |
| [MariaDB]     | 10.3, 10.2, 10.1   | `mariadb`       | [wodby/mariadb]                    |
| [PostgreSQL]  | 10, 9.x            | `postgres`      | [wodby/postgres]                   |
| [Redis]       | 4.0, 3.2           | `redis`         | [wodby/redis]                      |
| [Node.js]     | 9.11, 8.11, 6.14   | `node`          | [wodby/node]                       |
| [Varnish]     | 4.1                | `varnish`       | [wodby/wordpress-varnish]          |
| [Solr]        | 7.x, 6.6, 5.5      | `solr`          | [wodby/solr]                       |
| Elasticsearch | 6.x, 5.6, 5.5, 5.4 | `elasticsearch` | [wodby/elasticsearch]              |
| Kibana        | 6.x, 5.6, 5.5, 5.4 | `kibana`        | [wodby/kibana]                     |
| [Memcached]   | 1.5                | `memcached`     | [wodby/memcached]                  |
| [Webgrind]    | 1.5                | `webgrind`      | [wodby/webgrind]                   |
| [Blackfire]   | latest             | `blackfire`     | [blackfire/blackfire]              |
| [Rsyslog]     | latest             | `rsyslog`       | [wodby/rsyslog]                    |
| [AthenaPDF]   | 2.10.0             | `athenapdf`     | [arachnysdocker/athenapdf-service] |
| [Mailhog]     | latest             | `mailhog`       | [mailhog/mailhog]                  |
| [OpenSMTPD]   | 6.0                | `opensmtpd`     | [wodby/opensmtpd]                  |
| Adminer       | 4.3                | `adminer`       | [wodby/adminer]                    |
| phpMyAdmin    | latest             | `pma`           | [phpmyadmin/phpmyadmin]            |
| Portainer     | latest             | `portainer`     | [portainer/portainer]              |
| Traefik       | latest             | `traefik`       | [_/traefik]                        |

[Apache]: ../containers/apache.md
[AthenaPDF]: ../containers/athenapdf.md
[Blackfire]: ../containers/blackfire.md
[Mailhog]: ../containers/mailhog.md
[MariaDB]: ../containers/mariadb.md
[Memcached]: ../containers/memcached.md
[Nginx]: ../containers/nginx.md
[Node.js]: ../containers/node.md
[OpenSMTPD]: ../containers/opensmtpd.md
[PHP]: ../containers/php.md
[PostgreSQL]: ../containers/postgres.md
[Redis]: ../containers/redis.md
[Rsyslog]: ../containers/rsyslog.md
[Solr]: ../containers/solr.md
[Varnish]: ../containers/varnish.md
[Webgrind]: ../containers/webgrind.md

[_/traefik]: https://hub.docker.com/_/traefik
[arachnysdocker/athenapdf-service]: https://hub.docker.com/r/arachnysdocker/athenapdf-service
[blackfire/blackfire]: https://hub.docker.com/r/blackfire/blackfire
[mailhog/mailhog]: https://hub.docker.com/r/mailhog/mailhog
[phpmyadmin/phpmyadmin]: https://hub.docker.com/r/phpmyadmin/phpmyadmin
[portainer/portainer]: https://hub.docker.com/r/portainer/portainer
[wodby/adminer]: https://github.com/wodby/adminer
[wodby/elasticsearch]: https://github.com/wodby/elasticsearch
[wodby/kibana]: https://github.com/wodby/kibana
[wodby/mariadb]: https://github.com/wodby/mariadb
[wodby/memcached]: https://github.com/wodby/memcached
[wodby/node]: https://github.com/wodby/node
[wodby/opensmtpd]: https://github.com/wodby/opensmtpd
[wodby/php-apache]: https://github.com/wodby/php-apache
[wodby/postgres]: https://github.com/wodby/postgres
[wodby/redis]: https://github.com/wodby/redis
[wodby/rsyslog]: https://github.com/wodby/rsyslog
[wodby/solr]: https://github.com/wodby/solr
[wodby/webgrind]: https://hub.docker.com/r/wodby/webgrind
[wodby/wordpress-nginx]: https://github.com/wodby/wordpress-nginx
[wodby/wordpress-php]: https://github.com/wodby/wordpress-php
[wodby/wordpress-varnish]: https://github.com/wodby/wordpress-varnish
[wodby/wordpress]: https://github.com/wodby/wordpress
