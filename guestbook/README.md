
### Guestbook🔧

Comando para desplegar contenedor

```
docker-compose up -d
```

Una vez desplegado el contenedor, hacer clik derecho sobre la imagen guestbook-compose y pulsar Open in Browser

_archivo yml_

```
version: '3.1'
services:
  app:
    container_name: guestbook-compose
    image: iesgn/guestbook
    restart: always
    ports:
      - 80:5000
  db:
    container_name: redis-compose
    image: redis
    restart: always
```


_Archivos de referencia_

* [YML](https://josedom24.github.io/curso_docker_2022/sesion4/guestbook.html) - Usado para generar yml
