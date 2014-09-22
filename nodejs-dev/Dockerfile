FROM plause/nodejs

RUN apt-get update && apt-get -y upgrade
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install git
RUN apt-get clean && rm /var/lib/apt/lists/* -rf

RUN npm install -g yo gulp bower grunt-cli
