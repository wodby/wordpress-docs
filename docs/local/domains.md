# Domains Configuration

[Traefik](https://hub.docker.com/_/traefik) container used for routing. By default, we use port `8000` to avoid potential conflicts but if port `80` is free on your host machine just replace traefik's ports definition in the compose file.

Add `127.0.0.1 wp.docker.localhost` to your `/etc/hosts` file (some browsers like Chrome may work without it). Do the same for other default domains you might need from listed below:  

| Service      | Domain                                        |
| ------------ | --------------------------------------------- |
| nginx/apache | http://wp.docker.localhost:8000           |
| pma          | http://pma.wp.docker.localhost:8000       |
| adminer      | http://adminer.wp.docker.localhost:8000   |
| mailhog      | http://mailhog.wp.docker.localhost:8000   |
| varnish      | http://varnish.wp.docker.localhost:8000   |
| portainer    | http://portainer.wp.docker.localhost:8000 |
| webgrind     | http://webgrind.wp.docker.localhost:8000  |

You can modify domains under labels definition, e.g. `traefik.frontend.rule=Host:mailhog.wp.docker.localhost`.
