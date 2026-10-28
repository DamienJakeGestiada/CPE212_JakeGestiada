FROM ubuntu:24.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install -y apache2 mariadb-server && \
    rm -rf /var/lib/apt/lists/*

RUN printf '%s\n' '<html><body><h1>Activity 11 - Containerization</h1><p>Apache and MariaDB are installed.</p></body></html>' > /var/www/html/index.html

EXPOSE 80 3306

CMD ["bash", "-c", "service mariadb start && apachectl -D FOREGROUND"]
