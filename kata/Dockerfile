FROM php:8.0-apache
WORKDIR /var/www/html
COPY my-apache-site.conf /etc/apache2/sites-available/my-apache-site.conf
RUN echo "ServerName localhost" >> /etc/apache2/apache2.conf &&\
    a2enmod rewrite &&\
    a2dissite 000-default &&\
    a2ensite my-apache-site &&\
    service apache2 restart
EXPOSE 80
