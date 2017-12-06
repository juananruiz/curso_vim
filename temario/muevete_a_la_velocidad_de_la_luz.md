# Muévete a la velocidad de la luz

Vim te permite saltar a cualquier línea de un fichero de manera instantanea. Abre el fichero tal y cual. Pulsa 5G para ir a la línea 5, 10G para ir a la línea 10, etcétera. Si te resulta más cómodo también puedes usar 5gg, o 10gg, el resultado es el mismo. Recuerda que con gg a secas vas al principio del fichero, mientras que con G a secas vas al final.

Para ir rápidamente de un sitio a otro de un fichero es muy útil tener activada la numeración de líneas, esto se consigue con `:set number` desde la línea de comandos, pero es más cómodo ponerlo en tu fichero ".vimrc" para no tener que teclearlo cada vez. 

En algunos casos puede ser incluso más interesante utilizar la numeración relativa, esto se consigue con `:set relativenumber` 

## Aumenta tu velocidad sin perder puntos

Uno de los comandos más potentes de Vim es algo tan simple como el punto. Sí, sí, el `.`

El punto repite siempre la última acción que hayas hecho, repite acciones simples o atómicas, no secuencias de acciones, para eso tenemos las macros que veremos más adelante.

Por ejemplo si tecleas `dd` para borrar una línea, puedes borrar la siguiente con `.`

Si insertas o modificas una palabra o un grupo de palabras, puedes moverte hacía otro lugar del texto y repetir la inserción o modificación con el `.` 

Si tienes la siguiente frase:

"Tenemos seis manzanas y nos quitan dos manzanas, ¿cuántas manzanas nos quedan?"

Y quieres sustituir las manzanas por peras, podrías hacer:

`2w` para ir a la primera aparición de "manzanas".

`cw` para eliminar la palabra "manzanas" y entrar en modo insertar.

`peras` para escribir la palabra "peras" desde el modo inserción. 

Luego pulsas `<ESCAPE>` para volver a modo normal.

`5w` para ir a la siguiente aparición de "manzanas".

`.` para repetir el cambio. (Vim almacena la secuencia `cwperas` como una acción simple)

`3w` para la siguiente "manzanas"  y de nuevo `.` para cambiar por "peras".

Imagina que en vez de "peras" por "manzanas" tienes que cambiar "MaxRequestsPerChild" por "MaxSpareThreads" ¿cuántas correcciones te ahorrarías?

Ahora que has visto la potencia del punto, te animo a usarlo "a saco" con algún fichero de ejemplo para ver como funciona y cuales son sus limitaciones. Si quieres puedes usar el fichero del [ejercicio "lineas gemelas"](https://github.com/juananruiz/curso_vim/blob/master/ejercicios/lineas_gemelas.txt) para hacer de manera mucho más rápida ese primer ejercicio que hiciste sin conocer este nuevo comando.


## La línea de comandos

Cuando pulsas `:` para ejecutar un comando o `/` para realizar una búsqueda el cursor se va a la línea de comandos, que está en la parte inferior de la pantalla.

El modo comando permite algunos atajos de teclados sencillos para moverse por él, aquí si puedes usar los cursores (si los tienes disponibles, claro). Veamos algunos de estos atajos para ganar rapidez.

Para moverte por caracteres usa los cursores izquierda y derecha, si pulsas las teclas `SHIFT` o `CTRL` junto con estos cursores te moverás por palabras, para ir al principio de la línea pulsa `CTRL+b`, para irte al final pulsa `CTRL+e`. 

Los cursores arriba y abajo te permiten recorrer el historial de comandos (o de búsquedas) que has utilizado anteriormente. Si tecleas el comando `:hist` o `:history` podrás ver todo el listado del historial de comandos. Para ver el historial de búsquedas usa `:hist se` o `:history search` 

Si no te has cansado de trucos: 

* `CTRL+u` borra la línea completa
* `CTRL+w` borra una palabra
* `ESC` se sale del modo comando o búsqueda sin hacer nada

[<< Vuela como si no te afectara la gravedad](https://github.com/juananruiz/curso_vim/blob/master/temario/sobrevivir_al_primer_impacto.mdtemario/vuela_como_si_no_te_afectara_la_gravedad.md) - [Volver al índice](https://github.com/juananruiz/curso_vim) - [Vista de rayos X para búsquedas y sustituciones >>](https://github.com/juananruiz/curso_vim/blob/master/temario/vista_de_rayos_x_para_busquedas_y_sustituciones.md)
