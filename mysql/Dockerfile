FROM ubuntu:trusty

RUN apt-get update && apt-get -y upgrade
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install mysql-client
RUN rm /var/lib/apt/lists/* -rf

ADD etc/mysql/conf.d/default-charset.cnf /etc/mysql/conf.d/
