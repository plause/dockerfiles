## Apache2

Build a docker image for Apache web server.

### Build

    docker build -t daemon/apache .

### Usage

#### Serve static files

    docker run -d -v /path/to/files:/var/www/html daemon/apache

#### Add a new virtual host

    docker run -d -v /path/to/host.conf:/etc/apache2/sites-enabled/host.conf daemon/apache
