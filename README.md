# Frst-example-1
Apuntes importantes
## Estamos probando el manejo de diferenetes branch.
Para crear una rama tenemos que tener en cuenta que esta se crea en el lugar donde nos encontremos, para ubicarnos pordemos usar ```git status```, y ubicar el HEAD.
Luego podemos usar el comando para crear la rama que es ``` git branch cabcera``` a esta rama la llamamos cabecera. Despues de ejecutar el comando de creacion de la rama aparentemente no pasa nada en la consola, pero, para observar los cambios ejecutamos ```git show``` podemos obseravar las diferentes ramas.

Para movernos entre ramas se usa ```git checkout cabecera``` y ahi estaras dentro de la rama que especificaste.


Al momento de hacer un merge podemos generar conflictos, normalmente un merge se usa para unir los cambios de dos ramas en un documento final ``` git merge cabecera``` estando en main, usamos ese comando y hacemos un merge hacia cabecera.
Un problema comun es que se hayan hecho cambios en las mismas lineas de codigo y eso genera un conflicto, para solucionarlos VIsual estudio nos puede ayudar o tenemos que ver que cambios se tienen que descartar.

## Llaves publicas y llaves privadas

Para enviar mensajes cifrados se necesita el conocimiento del manejo de llaves publis y privadas, el receptor genera su llave publica y privada, luego comparte la llave publica a quien quiere enviar el mensaje, esta persona escribe el mensaje secreto y lo pasa por la llave publica, pase lo que pase, el unico que podra decifrar el mensaje es quien tenga la llave privada.
### Crear llave en git hub

Para crear la lleva nos debemos ubicar en home ~, ya que las llaves no son ni por repositorios, ni por archivo, son por personas

En caso de que queramos cambiar el correo de configuracion del git usamos ```git config --global user.email "tucorreo@gmail.com"``` y para poder mirar los cambios usamos ```git config -l```. El correo tiene que ser el mismo el cual tenemos vinculado el repositorio en git hub.

Para crear la llave usamos el comando ```ssh-keygen -t rsa -b 4096 -C "tucorreo@gmail.com"```
a continuacion te muestra la ubicacion de la llave en una carpeta oculta, tu puedes cambiarla si es tu deseo.
Una vez que tengas tu llave, la abres y la pones en git hub, pero antes tienes que probar que esten corriendo usando este comando ```eval $(ssh-agent -s)```
Para agregar la llave tenemos que recordar en donde esta ubicada y usar este comando ```ssh-add ~/.ssh/id_rsa```, debes tener cuidado de no compartir la llave privada.
