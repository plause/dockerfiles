FROM ubuntu:trusty

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get -y install mysql-server && rm /var/lib/apt/lists/* -rf

ADD etc/mysql/conf.d/bind-address.cnf /etc/mysql/conf.d/
ADD etc/mysql/conf.d/default-charset.cnf /etc/mysql/conf.d/
ADD etc/mysql/conf.d/init-file.cnf /etc/mysql/conf.d/
ADD etc/mysql/init.sql /etc/mysql/

EXPOSE 3306

CMD ["mysqld_safe"]
