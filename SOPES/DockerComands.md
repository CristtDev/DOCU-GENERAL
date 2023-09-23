# Crear imagen
docker build -t username/name_container .

# Crear y ejecutar contenedor
docker run --rm -it -p 8000:8000 username/name_container

# loggearse a dockerhub
docker login

# Subir imagen a docker hub
docker push username/name_container

# Clonar imagen de docker
docker pull imagenName

# Ver contenedores activos
docker ps

# Ver contenedores totales
docker ps -a

# Ver imágenes totales
docker images

# Eliminar contenedor
docker rm id_container

# Eliminar imagen
docker rmi id_image
