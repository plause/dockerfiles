## PHP FastCGI Process Manager

Build a docker image for PHP5 FPM daemon.

### Build

    docker build -t daemon/php5-fpm .

### Usage

#### Serve your PHP web application:

    docker run -d -p 9000 -v /path/to/dists:/var/projectname daemon/php5-fpm

#### Link your PHP FPM to a web server

    docker run -d --link your-php5-fpm-container:php5-fpm daemon/nginx
