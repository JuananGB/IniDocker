
# InicioDocker

### 1. Descarga la imagen 'ubuntu' y comprueba que está en tu equipo:

+ docker pull ubuntu (descargamos la imagen ubuntu).

+ docker images (Verificamos si la imagen se ha descargado correctamente).

### 2. Crear un contenedor sin ponerle nombre y verificar si está arrancado:

* docker run -d ubuntu (Creamos un contenedor sin un  nombre definido)

* docker ps (Comprobamos si está arrancando correctamente).

### 3. Crear un contenedor con el nombre 'dam_ubu1' y acceder a él:

* docker run -d --name dam_ubu1 ubuntu (Creamos un contenedor pero a diferencia de anteriormente , aquí si definimos un nombre "dam_ubu1").

* docker exec -it dam_ubu1 bash (Accedemos al contenedor)

### 4. Comprobar la dirección IP del contenedor 'dam_ubu1' y realizar un ping a google.com:

* ip a (Esto mostrará la dirección IP del contenedor)
* ping google.com (Comprueba si podemos acceder a google desde el contenedor).

### 5. Crear un contenedor con el nombre 'dam_ubu3' y realizar un ping entre contenedores:

* docker run -d --name dam_ubu3 ubuntu (Creamos un contenedor con el nombre "dam_ubu3").

* ping dam_ubu3 (Realizamos un ping con el nombre del contenedor)

### 6. Salir del terminal y verificar qué ocurrió con el contenedor:

Para salir del terminal dentro del contenedor y volver al sistema host, simplemente cierra la terminal o ejecuta el comando 'exit'.

Para verificar qué ocurrió con el contenedor después de salir, puedes ejecutar:

* docker ps -a

### 7. Sal del terminal. ¿Qué ocurrió con el contenedor?

Si sales del terminal sin detener el contenedor, el contenedor seguirá ejecutándose en segundo plano. Para salir del terminal sin detener el contenedor, simplemente cierra la ventana o la pestaña del terminal. El contenedor continuará en ejecución hasta que lo detengas manualmente.

### 8. ¿Cuánta memoria en el disco duro ocupaste?

Puedes verificar cuánto espacio en disco ocupan tus imágenes y contenedores con los siguientes comandos:

Para ver el uso de disco de imágenes:

- docker system df -v

Para ver el uso de disco de contenedores:

- docker ps -s

### 9. ¿Cuánta RAM ocupan los contenedores? ¿Hay algún comando de Docker para saber esto?

Para ver la cantidad de RAM que está utilizando cada contenedor, puedes utilizar el siguiente comando:

- docker stats (Este comando mostrará una lista de contenedores en ejecución junto con información sobre el uso de CPU, memoria y otros recursos).











 



