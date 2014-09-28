FROM ubuntu:trusty

RUN apt-get update && apt-get -y upgrade
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install mysql-server
RUN rm /var/lib/apt/lists/* -rf

ADD etc/mysql/conf.d/bind-address.cnf /etc/mysql/conf.d/
ADD etc/mysql/conf.d/default-charset.cnf /etc/mysql/conf.d/

VOLUME ["/var/lib/mysql", "/var/log/mysql", "/etc/mysql"]

CMD ["mysqld_safe"]

EXPOSE 3306
