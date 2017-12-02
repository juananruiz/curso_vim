# Muévete a la velocidad de la luz

Vim te permite saltar a cualquier línea de un fichero de manera instantanea. Abre el fichero tal y cual. Pulsa 5G para ir a la línea 5, 10G para ir a la línea 10, etcétera. Si te resulta más cómodo también puedes usar 5gg, o 10gg, el resultado es el mismo. Recuerda que con gg a secas vas al principio del fichero, mientras que con G a secas vas al final.

Para ir rápidamente de un sitio a otro de un fichero es muy útil tener activada la numeración de líneas, esto se consigue con `:set number` desde la línea de comandos, pero es más cómodo ponerlo en tu fichero ".vimrc" para no tener que teclearlo cada vez. 

En algunos casos puede ser incluso más interesante utilizar la numeración relativa, esto se consigue con `:set relativenumber`  

## La línea de comandos

Cuando pulsas `:` para ejecutar un comando o `/` para realizar una búsqueda el cursor se va a la línea de comandos, que está en la parte inferior de la pantalla.

El modo comando permite algunos atajos de teclados sencillos para moverse por él, aquí si puedes usar los cursores (si los tienes disponibles, claro). Veamos algunos de estos atajos para ganar rapidez.

Para moverte por caracteres usa los cursores izquierda y derecha, si pulsas las teclas `SHIFT` o `CTRL` junto con estos cursores te moverás por palabras, para ir al principio de la línea pulsa `CTRL+b`, para irte al final pulsa `CTRL+e`. 

Los cursores arriba y abajo te permiten recorrer el historial de comandos (o de búsquedas) que has utilizado anteriormente. Si tecleas el comando `:hist` o `:history` podrás ver todo el listado del historial de comandos. Para ver el historial de búsquedas usa `:hist se` o `:history search` 

Si no te has cansado de trucos: 

* `CTRL+u` borra la línea completa
* `CTRL+w` borra una palabra
* `ESC` se sale del modo comando o búsqueda sin hacer nada
