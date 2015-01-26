FROM runtime/nodejs

RUN apt-get update && apt-get -y install --no-install-recommends npm git && rm /var/lib/apt/lists/* -rf

ENTRYPOINT ["npm"]
