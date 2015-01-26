FROM develop/javac

RUN apt-get update && apt-get -y install maven && rm /var/lib/apt/lists/* -rf

ENTRYPOINT ["mvn"]
