## MySQL Server

Build a docker image for MySQL Server.
You can fetch the [automated build](https://registry.hub.docker.com/u/plause/mysqld/) of this image
from the public [Docker Hub Registry](https://registry.hub.docker.com/).

### Base Image

[ubuntu:trusty](https://registry.hub.docker.com/_/ubuntu/)

### Usage

The best practice of using this image is to build your own from it.
Here is an example dockerfile:

    FROM plause/mysqld

    # create a new database and a new user
    RUN mysql -e "CREATE SCHEMA tbd; GRANT ALL ON tbd.* TO 'user'@'host' IDENTIFIED BY 'password'"

    # save mysql data files
    VOLUME ["/var/lib/mysql"]

Build an image from the new dockerfile:

    docker build -t project/mysqld-tbd .

and use it like these:

#### Create a mysql instance for TBD:

    docker run -d -p 3306 --name tbd-mysql project/mysqld-tbd

#### Restart the mysql service for TBD:

    docker restart tbd-mysql
