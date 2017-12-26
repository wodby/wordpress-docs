# Quick start

!!! danger "Persistence of database data":
    You will lose MariaDB / PostgreSQL data if you run `docker-compose down`. Instead use `docker-compose stop` to stop containers. Alternatively, you can use a manual volume for mariadb data (see compose file), this way your data will always persist. 

There 2 options how to use docker4wordpress – you can either run [vanilla](https://en.wikipedia.org/wiki/Vanilla_software) WordPress from the image or mount your own WordPress codebase:

## Option 1: Run Vanilla WordPress from Image (default)

1. Download `docker-compose.yml` file from the [latest stable release](https://github.com/wodby/docker4wordpress/releases)
2. Run containers: `docker-compose up -d` (it may take some time for them to initialize) 
3. [Configure domains](domains.md) 
4. That's it! Proceed with WordPress installation at http://wp.docker.localhost:8000. Default database user, password and database name are all `wordpress`, database host is `mariadb`
5. You can see status of your containers and their logs via portainer at http://portainer.wp.docker.localhost:8000

## Option 2. Mount my WordPress Codebase

1. Download `docker-compose.yml` file from the [latest stable release](https://github.com/wodby/docker4wordpress/releases) to your WordPress project root
2. Replace php image from `wodby/wordpress` (PHP + vanilla WordPress) to `wodby/wordpress-php` (just PHP)
3. Update _nginx/apache_ and _php_ volumes to `- ./:/var/www/html` to mount your codebase
4. Ensure your wp-config.php has the same credentials as _mariadb_ service 
5. Optional: [import existing database](import-export.md)
7. Optional: uncomment lines in the compose file to run _redis_, _varnish_, _phpmyadmin (pma)_ 
8. [Configure domains](domains.md)
9. Run containers: `docker-compose up -d`
10. That's it! Your WordPress website should be up and running at http://wp.docker.localhost:8000
11. You can see status of your containers and their logs via portainer at http://portainer.wp.docker.localhost:8000

You can stop containers by executing:
```bash
docker-compose stop
```

Have a problem? Submit a new issue on [GitHub](https://github.com/wodby/docker4wordpress/issues) or ask [community on Slack](http://slack.wodby.com)

!!! tip "Permissions issues":
    To avoid potential problems with permissions between your host and containers please follow [these instructions](permissions.md)

!!! info "For macOS users":
    Docker for Mac volumes has poor performance. However there are workarounds, read more [here](docker-for-mac.md)

Feel free to adjust volumes and ports in the compose file for your convenience. 

