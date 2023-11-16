# WordPress Docker

Repositorio que permite el uso e instalación de wordpress, en un contenedor docker
para poder realizar pruebas, desarrollos en modo local sin tener que instalar un servidor de base ded atos
, un aplication server, configurarlo, etc.

Con este repositorio puedes usarlo como base para tu proyecto de sitio web en wordpres,
incluso tener varios docker con diferentes proyectos corriendo al mismo tiempo en tu computadora local.

# Requisitos #
Para poder utilizar el contener solo necesitas tener instalado docker engine y docker compose, mismos que vienen dentro
de la instalación de docker desktop para Mac, Windows y Linux.

# Modo De Uso #
 Para poder utilizar el contenedor deberás renombrar el archivo docker-compose.yaml.dist a docker-compose.yaml
 (una vez instalado Docker Desktop)
 
## Iniciar Servicio ##

En una terminal escribir

```
docker-compose up -d
```

## Detener Servicio ##

En una terminal escribir

```
docker-compose stop
```


# Explicación del Archivo Yaml #

## Servicios ##

### DataBase ### 

Comprende del contenedor con la base de datos mariadb instalada, este contenedor
tiene diversas variables de entorno que pueden ser modificables:

```
volumes:
      - db_data:/var/lib/mysql
```

Este es el volumen