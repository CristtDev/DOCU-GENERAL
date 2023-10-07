# COMANDO PARA CORRER EL NAMESPACE.YAML
* kubectl apply -f nombre-archivo
* kubectl get ns  (para obtener los namespaces creados)

# COMANDOS PARA CORRER LOS SERVICIOS
(Los servicios se encargaran de exponer un puerto hacia los contenedores)
targetPOrt es el puerto del contenedor
nodePOrt puerto en el nodo que apunta al contenedor
con el selector: busca los no pods con node wordpress y se ira a esos
* kubectl -n nombre-namespace apply -f nombre-archivo.yaml
* kubectl -n nombre-namespace get svc (ver los servicios en ese namespace)

# COMANDOS PARA CORRER EL DEPLOY
(crea cant de replicas de la imagen a crear)
targetPOrt es el puerto del contenedor por eso en el containerPort va igual 
* kubectl -n nombre-namespace apply -f nombre-archivo.yaml
* kubectl -n nombre-namespace get pods (ver los pods en ese namespace)
* kubectl -n nombre-namespace delete pod nombrePod 

# COMANDOS PARA BROWSEAR LOS NODOS
* kubectl get noes -o wide (para ver la ip publica del worker o nodo) para llegarle a la app +Puerto del servicio

------------------------------------------------------------------------------------
# GUIA PARA IMPLEMENTAR SERVICIO INGRESS
* kubectl apply -f . (crea todo el directorio para la configuracion del ingress)
* kubectl get ns
* kubectl -n nginx-ingress get all
* kubectl get ing (para ver las reglas de ingress)

# COMANDO PARA VER EN CONSOLA LAS APIS CORRIENDO
* curl v2.nombre.local:PORT