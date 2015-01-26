FROM ubuntu:trusty

RUN apt-get update && apt-get -y install nginx && rm /var/lib/apt/lists/* -rf

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
