# Going live

Make sure you check the following points before you go live with Wodby:

* [Auto backups](https://help.wodby.com/apps/backups) enabled and launch time is set to a less visited time gap (usually 01-06 am) 
* You have enough free disk space on your server considering your backups rotation period. You can always move Wodby's and applications'a data to an external volume, [see instructions](https://help.wodby.com/infrastructure/using-external-volumes-for-applications-data)
* If you use [git deployment](https://help.wodby.com/git/) workflow, it's recommended to use git tag instead of branch. If you prefer using branch, make sure auto deployment via git hooks is disabled
* You have a correct primary domain
* Your custom domains have enabled [SSL](https://help.wodby.com/apps/ssl)
* If you have SSL enabled on your domains, make sure you have HTTP to HTTPS redirect and HSTS enabled
* Disable technical domains
* Cron enabled
* Caching tools used: [redis](containers/redis.md) as an internal cache storage, [varnish](containers/varnish.md) as a caching reverse proxy 
* [OpenSMTPD](containers/opensmtpd.md) used in pair with a 3rd party SMTP service for guaranteed mail delivery
* Set up an external uptime monitoring (e.g. https://uptimerobot.com/, https://pingdom.com)