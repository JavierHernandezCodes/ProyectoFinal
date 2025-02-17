#Imagen base
FROM debian

LABEL org.opencontainers.image.authors="josejavierhernandez.alu@iespacomolla.es"

#Actualizaciones + instalación de VIM + instalación del servidor web NGINX + PHP
RUN apt update && \
    apt install -y apache2 php libapache2-mod-php-yaml php-mysql

# Habilito los módulos "rewrite" y "headers"
RUN a2enmod rewrite && \
    a2enmod headers

#Expongo el puerto de NGINX
EXPOSE 80

# Comando para iniciar Apache en primer plano
CMD ["apachectl", "-D", "FOREGROUND"]