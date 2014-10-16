FROM ubuntu:trusty

RUN apt-get update && apt-get -y upgrade
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y nginx
RUN apt-get clean && rm /var/lib/apt/lists/* -rf

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
