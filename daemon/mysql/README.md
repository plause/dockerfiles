## MySQL Server

### Build

    docker build -t daemon/mysql .

### Usage

#### Run the demo instance

    docker run -d -p 3306:3306 daemon/mysql

connect to the demo (default password is: pas$W0rd):

    mysql --host 172.17.42.1 --user root --port 3306 --password

Note, this instance is demo only.

#### Create your own instance

create an init SQL file with this content:

    CREATE SCHEMA IF NOT EXISTS dbname;
    GRANT ALL ON dbname.* TO 'dbuser'@'%' IDENTIFIED BY 'pas$W0rd';

and mount it to an instance:

    docker run -d -p 3306 -v /path/to/init.sql:/etc/mysql/init.sql daemon/mysql

then you can connect using this command:

    mysql --host docker_host --port docker_mapping_port --user dbuser --password

#### Save mysql server data

    docker run -d -p 3306 -v /var/lib/mysql daemon/mysql
