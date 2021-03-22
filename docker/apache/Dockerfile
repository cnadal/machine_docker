FROM php:7.4-apache
RUN curl -OL https://github.com/composer/composer/releases/download/2.0.11/composer.phar
RUN mv composer.phar /usr/local/bin/composer
RUN chmod +x /usr/local/bin/composer && a2enmod rewrite && service apache2 restart
RUN apt-get update && apt-get install -y nano
RUN apt-get install -y  git
# renseignez votre mail
RUN git config --global user.email "you@example.com"
# renseignez votre nom de user
RUN git config --global user.name "you"
RUN apt-get install -y wget
RUN wget https://get.symfony.com/cli/installer -O - | bash
RUN mv /root/.symfony/bin/symfony /usr/local/bin/symfony
RUN docker-php-ext-install pdo_mysql
RUN apt-get install -y zip
RUN apt-get install -y zlib1g-dev libicu-dev g++
RUN docker-php-ext-configure intl
RUN docker-php-ext-install intl

#RUN openssl req -new -newkey rsa:4096 -days 3650 -nodes -x509 -subj \
#"/C=nc/ST=fr/L=pe/O=nc/CN=toto.fr" \
#-keyout ./ssl.key -out ./ssl.crt

#RUN mkdir /etc/apache2/ssl
#RUN cp ./ssl.crt /etc/apache2/ssl/ssl.crt
#RUN cp  ./ssl.key /etc/apache2/ssl/ssl.key

RUN mkdir -p /var/run/apache2/
#RUN a2enmod ssl
#EXPOSE 80
#EXPOSE 443

