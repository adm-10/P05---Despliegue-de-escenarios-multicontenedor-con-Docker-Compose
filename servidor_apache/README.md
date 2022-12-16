
### Servidor Apache 🔧

Comando para desplegar contenedor

```
docker-compose up -d
```

Una vez desplegado el contenedor, hacer clik derecho sobre la imagen httpd:lastest y pulsar Open in Browser

_archivo yml_

```
version: '3.1'
services:
  apache:
    image: httpd:latest
    container_name: my-apache-app
    ports:
    - '8080:80'
    volumes:
    - ./website:/usr/local/apache2/htdocs
```
_Se creo una carpeta website, con la ruta donde se alojaran el htdocs_


_Archivos de referencia_

* [YML](https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/Simple-Apache-docker-compose-example-with-Dockers-httpd-image) - Usado para generar yml
