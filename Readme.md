

# Documentación docker

- Versión instalada de docker
```docker --version```

- Ver la información general de docker
```docker info```

## Imagen

- Descargar una imagen
```docker pull [nombre imagen : version]```
```docker pull mysql:8.0```

- Ver el listado de imagenes 
```docker images```

- Eliminar una imagen
``` docker rmi [nombre/id]```
```docker rmi mysql```

- Construir una imagen desde un Dockerfile
```docker build -t [nombre] [ubicación]```
```docker build -t mi_imagen .```

## Contenedores

- Crear y ejecutar un contenedor
```docker run -d --name [nombre contenedor] -p [host:contenedor] [nombre imagen]```

```docker run -d --name mi_contenedor -p 3000:80 nginx```

- Listar contenedores en ejecución
```docker ps```
- Listar contenedores 
```docker ps -a```

- Detener un contenedor
```docker stop [nombre /id]```
```docker stop mi_contenedor```

- Eliminar un contedor (detenido)
```docker rm [nombre / id]```
```docker rm mi_contenedor```

- Eliminar forzando su detención
```docker rm -f [nombre / id]```

- Iniciar un contenedor
```docker start [nombre / id]```

- Reiniciar contenedor
```docker restart [nombre / id]```

- Limpia TODO lo que no se esté usando
```docker system prune``` 


# Docker compose

- Leventar servicios definidos en el docker-compose.yml
```docker compose up -d```
- Detener servicios
``` docker compose down```