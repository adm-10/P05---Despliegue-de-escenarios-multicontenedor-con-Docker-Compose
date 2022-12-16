
### Adminer 🔧

Comando para desplegar contenedor

```
docker-compose up -d
```

Una vez desplegado el contenedor, hacer clik derecho sobre la imagen adminer pulsar Open in Browser


```
usuario: root
contraseña: example
```

_archivo yml_

```

version: '3.1'

services:

  adminer:
    image: adminer
    restart: always
    ports:
      - 8080:8080

  db:
    image: mysql:5.6
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: example

```
_Archivos de referencia_

* [YML](https://hub.docker.com/_/adminer) - Usado para generar yml
