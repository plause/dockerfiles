FROM ubuntu:trusty

RUN apt-get update && apt-get -y install apache2 && rm /var/lib/apt/lists/* -rf

EXPOSE 80

CMD ["apachectl", "-D", "FOREGROUND", "-k", "start"]
