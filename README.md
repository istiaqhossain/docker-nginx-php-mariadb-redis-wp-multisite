# Docker Nginx PHP Mariadb Redis WordPress

## Redis

Normally, Redis should work out-of-the-box with WordPress as long as it is accessible via localhost:6379.

The thing is, in a docker setup the redis instance is accessible via its container name.

So in order for WordPress to find it, you need to modify the constant in your wp-config.php file.

```
define( 'WP_REDIS_HOST', 'redis' );
define( 'WP_REDIS_PORT', '6379' );
```
