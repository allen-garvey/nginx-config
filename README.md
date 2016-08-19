# nginx Configuration

Configuration for nginx with php-fpm on FreeBSD (FEMP stack). Based on [digitalocean docs.](https://www.digitalocean.com/community/tutorials/how-to-install-an-nginx-mysql-and-php-femp-stack-on-freebsd-10-1)

## Dependencies

* FreeBSD 10.3
* nginx 1.10.1
* php-fpm 70

## Getting Started on FreeBSD

* Install latest versions of nginx, php-fpm and php-fpm extensions using pkg
* Create a file at `/usr/local/etc/nginx/nginx.conf` using the appropriate nginx configuration file
* Create a directory for nginx log files at `/var/log/nginx` if it doesn't exist, and change owner of that directory to `www` with `sudo chown www: /var/log/nginx`
* Change group and permissions for web directory to allow nginx access `sudo chown -R "$USER":www /webdirectory  && sudo chown -R 0755 /webdirectory`
* For php-fpm, create the file `/usr/local/etc/php-fpm.d/www.conf` using the file located in this repo at `freebsd/php-fpm/www.conf`
* Replace `/usr/local/etc/php.ini` with the php.ini file from this repo
* Start nginx and php-fpm

## License

nginx Configuration is released under the MIT License. See license.txt for more details.