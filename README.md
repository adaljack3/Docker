# Docker
Show Docker examples 

https://www.hostinger.es/tutoriales/como-instalar-y-usar-docker-en-ubuntu

Install Visual Studio Code

https://code.visualstudio.com/

sudo docker run -d -e POSTGRES_PASSWORD=password postgres  #Descarga postgres si no está en el equipo
-d es para mandarlo al background
-e es para establecer variable de entorno necesaria en esta imagen 

sudo docker images #muestra las imagenes que hay en el equipo de docker

sudo docker ps  #lista los contenedores 

>TAGS y nombres 

sudo docker run -d -e POSTGRES_PASSWORD=password postgres:bullseye  #Usa el tag especifico 

:. Se pueden correr distintas versiones de postgres sin causar conflicto porque existe AISLAMIENTO en docker


sudo docker run -d -e POSTGRES_PASSWORD=password --name bulleye_container postgres:bullseye  # crea un contenedor con un NOMBRE especifico  

No se pueden crear 2 contenedores con el mismo nombre

sudo docker ps  #lista contenedores ACTIVOS

sudo docker ps -a #Lista TODOS los contenerodes en el equipo 

>Eliminar Contenedores 

sudo docker rm    <container_ID>  #elimina el contenedor por ID 

sudo docker rm e78eff455669 38eee5c2a386  #Tambien puede eliminar varios contenedores

sudo docker rm NAME   #Tambien se puede eliminar por nombre

sudo docker rm -f 

sudo rm -f efadb5bdef25  #Fuerza la eliminación de un contenedor que esté en ejecución 

>Eliminar Imagenes

sudo docker images  #Lista las imagenes 

sudo rmi <IMAGE_ID>  #Elimina esa imagen, si hay un contenedor activo con esa imagen no permitirá eliminarla :. Eliminar primero el contenedor 

sudo rmi -f <IMAGE_ID>  #forzar la eliminación de una imagen  , no se pueden eliminar imagenes con un ID duplicado

sudo rmi -f REPOSITORY:TAG  #si exisen varias imagenes con el mismo ID pero con diferente TAG




