## Nginx

Build a docker image for Nginx daemon.

### Build

    docker build -t daemon/nginx .

### Usage

#### Serve static files

    docker run -d -v /path/to/files:/usr/share/nginx/html daemon/nginx

#### Add a new site configuration

    docker run -d -v /path/to/site.conf:/etc/nginx/sites-enabled/site.conf daemon/nginx

A sample `site.conf`:

    server {
      location ~ \.php$ {
        fastcgi_pass php-fpm:9000;
        include fastcgi_params;
      }
    }
