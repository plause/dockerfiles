FROM plause/java

RUN apt-get update && apt-get -y upgrade
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y tomcat7
RUN apt-get clean && rm /var/lib/apt/lists/* -rf

ENV CATALINA_BASE /var/lib/tomcat7
ENV CATALINA_TMPDIR /tmp

USER tomcat7

EXPOSE 8080

WORKDIR /usr/share/tomcat7

CMD ["bin/catalina.sh", "run"]
