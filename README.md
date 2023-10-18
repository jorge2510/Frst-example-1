# Frst-example-1
Apuntes importantes
## Estamos probando el manejo de diferenetes branch.
Para crear una rama tenemos que tener en cuenta que esta se crea en el lugar donde nos encontremos, para ubicarnos pordemos usar ```git status```, y ubicar el HEAD.
Luego podemos usar el comando para crear la rama que es ``` git branch cabcera``` a esta rama la llamamos cabecera. Despues de ejecutar el comando de creacion de la rama aparentemente no pasa nada en la consola, pero, para observar los cambios ejecutamos ```git show``` podemos obseravar las diferentes ramas.

Para movernos entre ramas se usa ```git checkout cabecera``` y ahi estaras dentro de la rama que especificaste.


Al momento de hacer un merge podemos generar conflictos, normalmente un merge se usa para unir los cambios de dos ramas en un documento final ``` git merge cabecera``` estando en main, usamos ese comando y hacemos un merge hacia cabecera.
Un problema comun es que se hayan hecho cambios en las mismas lineas de codigo y eso genera un conflicto, para solucionarlos VIsual estudio nos puede ayudar o tenemos que ver que cambios se tienen que descartar.