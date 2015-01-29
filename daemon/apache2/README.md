## Apache2

Build a docker image for Apache2 web server.

### Build

    docker build -t daemon/apache2 .

### Usage

#### Serve static files

    docker run -d -v /path/to/files:/var/www/html daemon/apache2

#### Add a new virtual host

    docker run -d -v /path/to/host.conf:/etc/apache2/sites-enabled/host.conf daemon/apache2
