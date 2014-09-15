FROM ubuntu:trusty

RUN apt-get update && apt-get -y upgrade
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y nginx
RUN apt-get clean && rm /var/lib/apt/lists/* -rf

VOLUME ["/etc/nginx", "/var/log/nginx", "/usr/share/nginx/html"]

EXPOSE 80

CMD ["nginx", "-c", "/etc/nginx/nginx.conf", "-g", "daemon off;"]
