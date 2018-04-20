# Quick start

There are 2 options how to use docker4wordpress – you can either run [vanilla](https://en.wikipedia.org/wiki/Vanilla_software) WordPress from the image or mount your own WordPress codebase:

## Option 1: Run Vanilla WordPress from Image

1. Clone [docker4wordpress repository](https://github.com/wodby/docker4wordpress) and switch to the [latest stable tag](https://github.com/wodby/docker4wordpress/releases) or download/unpack the source code from the [latest release](https://github.com/wodby/docker4wordpress/releases)
2. [Configure domains](domains.md)
3. From project root directory run `docker-compose up -d` or `make up` to start containers. Give it 10-20 seconds to initialize after the start
4. That's it! Proceed with WordPress installation at http://wp.docker.localhost:8000. Default database user, password and database name are all `wordpress`, database host is `mariadb`
5. You can see status of your containers and their logs via portainer: http://portainer.wp.docker.localhost:8000

## Option 2. Mount my WordPress Codebase

1. Download `docker4wordpress.tar.gz` from the [latest stable release](https://github.com/wodby/docker4wordpress/releases) and unpack to your WordPress project root. If you choose to clone [the repository](https://github.com/wodby/docker4wordpress) delete `docker-compose.override.yml` as it's used to deploy vanilla WordPress
2. Ensure database credentials match in your `wp-config.php` and `.env` files 
3. [Configure domains](domains.md)
4. Optional: [import existing database](import-export.md)
5. Optional: uncomment lines in the compose file to run [redis](../containers/redis.md), [varnish](../containers/varnish.md), phpmyadmin, etc
8. Optional: macOS users please read [this](docker-for-mac.md)
9. Optional: Windows users please read [this](permissions.md#windows)
10. Run containers: `docker-compose up -d` or `make up` (see all [make commands](make-commands.md))
11. That's it! Your WordPress website should be up and running at http://wp.docker.localhost:8000
12. You can see status of your containers and their logs via portainer: http://portainer.wp.docker.localhost:8000

!!! info "Optional files"
    If you don't need to [run multiple projects](multiple-projects.md) and don't use [docker-sync to improve volumes performance on macOS](docker-for-mac.md) feel free to delete `traefik.yml` and `docker-sync.yml` that come with the `docker4wordpress.tar.gz`

You can stop containers by executing `docker-compose stop` or `make stop`

Have a problem? Submit a new issue on [GitHub](https://github.com/wodby/docker4wordpress/issues) or ask [community on Slack](http://slack.wodby.com)

Feel free to adjust volumes and ports in the compose file for your convenience. 
