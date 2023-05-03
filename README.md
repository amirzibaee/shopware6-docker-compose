# shopware6-docker-compose
a docker-compose.yml for shopware 6


## Sample docker environment for shopware 6
This is a sample docker environment for shopware 6. It contains a docker-compose file with a php apache container, a mysql container and a phpmyadmin container.


```bash
# PHP Apache Docker
PHP_VERSION=7.4
APACHE_VERSION=2.4.32
APACHE_EXTERN_PORT=8000
PROJECT_ROOT=./shopware/

# Mysql Docker
MYSQL_VERSION=mariadb:10.5.18
MYSQL_EXTERN_PORT=3306
DB_ROOT_PASSWORD=root
DB_NAME=shopware
DB_USERNAME=shopware
DB_PASSWORD=shopware
DB_DATA_PATH=./mysql/data

# phpMyAdmin
PMA_EXTERN_PORT=8009
```

## FIX Permission
```bash
sudo chmod -R 777 folder/
```

## FIX jwt permission
```bash
sudo chmod -R 660 shopware/config/jwt/public.pem
sudo chmod -R 660 shopware/config/jwt/private.pem
# -> in docker container
chown www-data:www-data config/jwt/public.pem
chown www-data:www-data config/jwt/private.pem
```