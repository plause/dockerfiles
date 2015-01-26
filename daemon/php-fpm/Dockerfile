FROM ubuntu:trusty

RUN apt-get update && apt-get -y install php5-fpm && rm /var/lib/apt/lists/* -rf
ADD etc/php5/fpm/pool.d/www.conf /etc/php5/fpm/pool.d/

EXPOSE 9000

CMD ["php5-fpm", "-F"]
