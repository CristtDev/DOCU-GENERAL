# LISTAR BASES DE DATOS
* config get databases

# ENTRAR A BASE DE DATOS LOGICA
* Select [index]

# ESTABLECE UN CLAVE-VALOR  
* set [key] [value]

# OBTENER UN CLAVE-VALOR
* get [key]

# AGREGAR ELEMENTOS A ARREGLOS
* ZADD [key] [score XX!NX] [value]  

# INCREMENTAR CONTADORES DE ARREGLOS
* HINCRBY [key] [valor] [increment]

# OBTENER VALORES Y CONTEOS
* HGETALL [key]

# ELIMINAR ELEMENTOS DE ARREGLOS
* ZREM array [key]

# LISTAR ELEMENTOS DE ARREGLOS
* ZRANGE [key] [start] [stop]

----

## INSTALACION DE REDIS EN LOCAL 
* docker pull redis

## EJECUCION DE REDIS EN LOCAL
* docker run --name redis -p 6379:6379 -d redis

## EJECUCION DE REDIS EN LOCAL via CLI
* docker run -it --link redis:redis --rm redis redis-cli -h redis -p 6379

* docker run -it --network  --rm redis redis-cli -h redis -p 6379