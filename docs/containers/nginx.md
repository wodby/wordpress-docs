# Nginx

You can configure Nginx via environment variables that listed at https://github.com/wodby/wordpress-nginx

## Additional configuration

If the default wordpress config and available environment variables are not enough for your customizations you can replace the config with your own:

1. Copy `/etc/nginx/conf.d/wordpress.conf` to your codebase, adjust to your needs
2. Deploy code with your config file
3. Add new environment variable `NGINX_CONF_INCLUDE` for nginx service, the value should the path to your *.conf file (e.g. `/var/www/html/nginx.conf`
