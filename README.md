# CertiDevOps - DjangoRest - Docker

## Datos del estudiante
- Nombre: Marcos Andrés Simon Ágreda
- Código: 56728
- Materia: Certificación DevOps

## Descripción 

El presente proyecto, combina la utilización de tanto un Dockerfile, como de un archivo .yml Docker Compose para la creación de dos contenedores, uno para el almacenamiento de una API Rest, creada en el framework "Django" de Python, y otro para el almacenamiento de una base de datos "MySQl", con la cual, el contenedor anterior podrá conectarse.

El contenedor con el framework Django, tiene su acceso mediante el puerto 8001, teniendo como único endpoint el "/api/notes", el cual es accesible mediante el propio navegador.

EL contenedor con la base de datos MySQL, tiene su acceso mediante el puerto 3307.

## Instrucciones de uso

- Para poder ejecutar el proyecto, se debe tener instalado Docker y Docker Compose.
- Posteriormente, se debe clonar el repositorio en la carpeta deseada, mediante el comando: `git clone`
- Una vez clonado, ingresar al archivo Dockerfile, y escoger alguna de las dos opciones:
  - Mantener la opción de `image: marcosht4/django-rest:0.1` para obtener la imagen de DockerHub.
  - Cambiar dicha opción por `build: .` para obtener la imagen de manera local, mediante la construcción del Dockerfile (ADVERTENCIA: Debido a la inseguridad de no saber si los servidores de apt-get están disponibles, este proceso puede fallar fácilmente).
- Una vez escogida la opción, se debe ejecutar el comando `docker-compose up` para que se creen los contenedores.
- Esperar a que el mensaje de "Watching for file changes with StatReloader" del contenedor de Django aparezca, y posteriormente, ingresar a la dirección `localhost:8001/api/notes` mediante un navegador para poder acceder a la API Rest.
- Se le mostrará una página web, en dónde se podrán introducir datos, y posteriormente, dichos datos será almacenados en la base de datos MySQL.

