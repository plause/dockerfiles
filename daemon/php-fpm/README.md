## PHP FastCGI Process Manager

Build a docker image for PHP FPM daemon.

### Build

    docker build -t daemon/php-fpm .

### Usage

#### Serve your PHP web application:

    docker run -d -p 9000 -v /path/to/dists:/var/projectname daemon/php-fpm

#### Link your PHP FPM to a web server

    docker run -d --link your-php-fpm-container:php-fpm daemon/nginx
