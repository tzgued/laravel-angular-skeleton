

FROM webdevops/php-apache

LABEL author="Taha ZGUED" 

#RUN apt-get install -y apache2 php7.0 libapache2-mod-php7.0 && a2query -m php7.0 && a2enmod php7.0

RUN apt update && apt install -y php libapache2-mod-php
RUN apt update && apt install -y nodejs npm
RUN npm install -g @angular/cli  && npm cache clean --force
RUN apt install npm
#RUN service php-fpm stop

#COPY ports.conf /etc/apache2/ports.conf

WORKDIR /var/www/html/

RUN service apache2 restart

EXPOSE 4200