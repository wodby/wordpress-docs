# Varnish

You can configure Varnish via environment variables that listed at https://github.com/wodby/wordpress-varnish. 

Integration:

1. Go to `App instance > Stack > Varnish` in Wodby dashboard and copy automatically generated value of `$VARNISH_PURGE_KEY`
2. Install and activate [Varnish Caching plugin](https://wordpress.org/plugins/vcaching) in your WordPress website
3. On the plugin cache settings configure as shown below:  
    ![Varnish Caching plugin settings](/assets/wp-varnish-caching-plugin-settings.png)
4. Copy/paste the key to `Purge key` in plugin setting 
5. Save all plugin settings changes