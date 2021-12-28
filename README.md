# docker-kali-xfce
Imagen de kali con un script <<install.sh>> en su raiz <</>> el cual nos instala un server xrdp y xfce para una interfaz gráfica
al cual podemos acceder con cualquier herramienta de escritorio remoto por el puerto 3390 de nuestro pc, debemos tener instalado docker.

### Abrimos una terminal

"este paso es opcional, ya que con el siguiente, si no tienen la imagen en local, la descarga"

**docker pull cubanoar/kali** 

## Creamos el contenedor

**docker run -it -p 3390:3389 --name kali_xfce cubanoar/kali:v1**

## Dentro del contenedor

**./install.sh**

Lleva un poco de tiempo y le debemos pasar algunas elecciones como la configuracion del teclado 

Abrimos cualquier herramienta para conectarnos a un escritorio remoto, en W10 podemos ir a Inicio y buscar escritorio, nos va a salir una aplicación de conexión

**user:root**

**passwd:root**


Listo tenemos KaliLinux corriendo en un contenedor con interfaz gráfica y todo, lo podemos hacer con otras distros tambien!!!!

A la hora de correr de nuevo el kali, no usamos el <<run>>, lo hacemos asi:

**docker start -i kali_xfce**

Por las dudas le pasamos el siguiente comando para el server xrdp
 
 **service xrdp force-reload**
 
Abrimos cualquier herramienta para conectarnos a un escritorio remoto, en W10 podemos ir a Inicio y buscar escritorio, nos va a salir una aplicación de conexión
