FROM debian

ENV DEBIAN_FRONTEND=noninteractive

LABEL maintainer="davidgarciavalero@gmail.com"

RUN apt-get update && apt-get install -y \
    apache2 \
    php \
    php-mysql \
    php-yaml \
    && apt-get clean

RUN a2enmod rewrite headers

RUN mkdir -p /var/log/apache2/custom

WORKDIR /var/www/html

EXPOSE 80

CMD ["apachectl", "-D", "FOREGROUND"]
