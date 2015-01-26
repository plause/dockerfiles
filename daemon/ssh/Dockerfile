FROM ubuntu:trusty

RUN apt-get update && apt-get -y install openssh-server && rm /var/lib/apt/lists/* -rf
RUN mkdir /var/run/sshd

CMD ["/usr/sbin/sshd", "-D"]

EXPOSE 22
