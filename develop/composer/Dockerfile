FROM runtime/php5

RUN php -r "readfile('https://getcomposer.org/installer');" | php -- --install-dir=/usr/local/bin --filename=composer

ENTRYPOINT ["composer"]
