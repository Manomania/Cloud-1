FROM wordpress:php8.2-fpm


RUN apt-get update -y && apt-get install curl -y

RUN curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar \
&& chmod +x wp-cli.phar && \
mv wp-cli.phar /usr/local/bin/wp