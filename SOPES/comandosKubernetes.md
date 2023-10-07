# INSTALACION GCLOUD
* enlace docu: https://cloud.google.com/sdk/docs/install

-------

* Nota: tomar en cuenta al momento de instalar el cli as package source: si la distribucion soporta o no el signed-by

# CREACION CLUSTER
* gcloud init
* Escoger usuario y proyecto
* Establecer zona: uscentral1-a
* gcloud container clusters create api-cluster  --num-nodes 2 --machine-type n1-standard-2 --zone us-central1-f


----
* Nota: para el tipo de maquina se usan para el P2 (n2, n2d, n1)

# VERIFICACION CORRECTA INSTALACION 
gcloud --version

# VER INFO DE NODO 
kubectl get nodes -o wide

# CONECTARSE AL KLUSTER DESDE LA SHELL CUANDO HAY VARIOS
* gcloud container clusters get-credentials nombre-cluster --zone us-west1-a

# CONSTRUCCION DE IMAGEN EN CLUSTER
* docker build -t gcr.io/id_proyectoGoogle/nombre-imagen:tag .
 * docker push gcr.io/id_proyectoGoogle/nombre-imagen:tag

 * NOTA: luego para ver la imagen es en el buscador/container registry

# DARLE DEPLOY AL CONTENEDOR CREADO
* kubectl create namespace nombreSpace 
(namespace - apartado pa grupos )


# CONFIGURACIONES BASICAS
 * You can change it by running [gcloud config set compute/region NAME]. CAMBIO DE ZONA HORARIA
 * gcloud services enable container.googleapis.com (COMANDO POR UN ERROR AL CREAR EL KUBERNETE Y TIRA 400)
 * gcloud config list (para ver los detalles de la configuracion)
 * gcloud auth configure-docker (comando para habilitar autorizacion de push en cluster)
 * gcloud container clusters get-credentials "api-cluster" --zone us-central1-f (commndo para configurar zona y que permita crear el namespace)


# puertos
ports: Define los puertos del servicio. En este caso, se define un solo puerto, el puerto 3000.
port: El puerto del servicio en el clúster.
targetPort: El puerto del contenedor al que se dirige el tráfico del servicio.
nodePort: El puerto expuesto en cada nodo del clúster.
