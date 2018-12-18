# Redes
Por defecto, al instalar Docker en Linux se crea una interfaz de red virtual llamada `docker0` en el equipo host.

El comando `docker network` permite interactuar con las redes de Docker y los contenedores dentro de ellas, unos comandos importantes a tomar en cuenta son:
* Permite crear una red.
```
docker network create [nombre de la red]
```
* Permite conectar un contenedor de una red.
```
docker network connect
```
* Lista las redes existentes.
```
docker network ls
```
* Permite eliminar una red.
```
docker network rm
```
* Permite desconectar un contenedor de una red.
```
docker network disconnect
```
* Muestra información de interés sobre las redes de Docker.
```
docker network inspect
```
* Utilizar esta bandera al crear un contenedor permite especificar la red en la cual estará dicho contenedor.
```
--net [nombre de la red]
```
* Permite enlazar un contenedor a una red y así acceder a ellos por medio de su nombre.
```
--link [nombre del contenedor]
```

La red `bridge` es la que utilizan todos los contenedores por defecto, la host permite que los contenedores compartan la misma IP que la del equipo host.