# Buffers, ventanas y pestañas

Cada vez que abras un fichero en vim este se abre en un buffer, una especie de espacio de memoria en el que se carga el contenido del fichero. Los buffers se usan también para mostrar la ayuda (otro fichero al fin y al cabo) o para mostrar la estructura de directorios cuando usas `e.` o `:Ex`. Estos dos últimos casos tienen el atributo de no modificables, aunque puedes moverte por ellos, buscar, seleccionar y copiar texto como en cualquier otro buffer. 

Para poder visualizar un buffer necesitas una ventana, puedo tener una sola ventana pero varios buffers abiertos. Puedes reutilizar la misma ventana para ver el contenido de todos los buffers. Si abro una segunda ventana, la pantalla de vim se parte en dos mitades para mostrar cada una de ellas, ya sea mediante una divisoria horizontal `:split` o vertical `:vsplit`. Un mismo buffer puede estar en dos o más ventanas. Puedes seguir partiendo la pantalla en más ventanas hasta que prácticamente sólo te quepa una letra en cada una. 

A su vez las ventanas se pueden cargar en distintas pestañas, las pestañas te permiten tener distintas configuraciones de ventanas.

En cualquier caso la lista de buffers abiertos es global y puedes acceder a ellos desde cualquier ventana o pestaña

## Comandos para Buffers

`:ls` : lista todos los buffers que tienes abiertos

`:b1` te lleva al buffer marcado como **1** en la lista

`:b filename` : Nos lleva al buffer llamado filename. Este comando permite autocompletar pulsando <TAB>.

`CTRL-6` : Nos lleva al buffer del que venimos (atajo de :b#). 

`:bn` / `:bp` : Va al siguiente / anterior buffer de la lista de buffers.

`:bd`  Elimina el buffer de la lista de buffers y cierra la ventana donde estaba si no era la última

`:wall`  guarda los cambios en todos los buffers.

`:sba`  abre todos los buffers que tengamos en la lista de buffers dividiendo la pantalla para que quepan todos.

`:Ex`  abre el explorador de ficheros en la pantalla actual.

`:set hidden`  para trabajar cómodamente con múltiples buffers es imprescindible activar esta opción. Si no, no nos permite abandonar un buffer sin guardarlo previamente.


## Comandos para Ventanas

`:split`  nueva ventana horizontal 

`:vsplit`  nueva ventana vertical

`:sp fichero` abre el fichero en una nueva ventana horizontal

`CTRL-W CTRL-W`: siguiente ventana

`CTRL-W j, l, k, h` ir a la ventana en la dirección indicada

`CTRL-W =` : pone todas las ventanas al mismo tamaño

`CTRL-W c` : cerrar ventana (nunca cierra la última). Para acordarme pienso: "¡al WC!".

`close`  cerrar ventana (nunca cierra la última)

`q` cerrar ventana, si es la última sales de vim

`CTRL-W o`: cerrar todas las ventanas excepto la actual


## Comandos para Pestañas o Tabs

 `:tabnew` → abrir una nueva pestaña en blanco 

 `:tabedit <fichero>`  → abrir pestaña con un fichero cargado

`:tabnext` o `:tabn`  →   moverte a la siguiente pestaña


## Ejercicios con buffers, ventanas y pestañas

Parte la pantalla de vim en cuatro cuadros en cruz usando los comandos de ventanas

Carga en cada una de las ventanas un buffer distinto

Abre una nueva pestaña y carga los cuatro buffers usando sólo dos comandos

