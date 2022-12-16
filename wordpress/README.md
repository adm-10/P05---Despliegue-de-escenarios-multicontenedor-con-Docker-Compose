
### Wordpress🔧

Comando para desplegar contenedor

```
docker-compose up -d
```

Una vez desplegado el contenedor, hacer clik derecho sobre la imagen wordpress y pulsar Open in Browser

_archivo yml_

```
version: '3.1'
services:
  wordpress:
    container_name: servidor_wp-compose
    image: wordpress
    restart: always
    environment:
      WORDPRESS_DB_HOST: db
      WORDPRESS_DB_USER: user_wp
      WORDPRESS_DB_PASSWORD: asdasd
      WORDPRESS_DB_NAME: bd_wp
    ports:
      - 80:80
    volumes:
      - wordpress_data:/var/www/html/wp-content
  db:
    container_name: servidor_mysql-compose
    image: mariadb
    restart: always
    environment:
      MYSQL_DATABASE: bd_wp
      MYSQL_USER: user_wp
      MYSQL_PASSWORD: asdasd
      MYSQL_ROOT_PASSWORD: asdasd
    volumes:
      - mariadb_data:/var/lib/mysql
volumes:
    wordpress_data:
    mariadb_data:

```
_Archivos de referencia_

* [YML](https://josedom24.github.io/curso_docker_2022/sesion4/wordpress.html) - Usado para generar yml

