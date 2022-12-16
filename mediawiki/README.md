

### Mediawiki 🔧

Comando para desplegar contenedor

```
docker-compose up -d
```

Una vez desplegado el contenedor, hacer clik derecho sobre la imagen mediawiki y pulsar Open in Browser

_archivo yml_

```
version: '3.2'
services:
  web:
    image: mediawiki
    ports:
      - 80:80
    volumes:
      #- ./LocalSettings.php:/var/www/html/LocalSettings.php
      - database:/var/www/data
      - images:/var/www/html/images
volumes:
    database:
    images:
```
_Archivos de referencia_

* [YML](https://www.mediawiki.org/wiki/Docker/Hub) - Usado para generar yml
