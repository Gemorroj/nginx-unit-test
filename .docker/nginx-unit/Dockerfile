FROM nginx/unit:1.26.0-php8.0

RUN apt update -y \
    && apt upgrade -y \
    && apt install unzip -y \
    # && apt install php-xml -y \
    && apt clean -y


# Composer
RUN curl -L -o /composer.phar https://github.com/composer/composer/releases/download/2.1.14/composer.phar \
    && chmod 755 /composer.phar


COPY ./unit.json /docker-entrypoint.d/
WORKDIR /var/www/app
