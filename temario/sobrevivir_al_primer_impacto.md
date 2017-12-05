# Sobrevivir al primer impacto

Dice Elon Musk (el fundador de Tesla, SpaceX, etc) que él quiere morir en Marte, pero no del primer impacto. Eso quiero conseguir en esta sesión, que sobrevivas al primer impacto con Vim y no salgas corriendo del curso nada más abrir el editor por primera vez.

Así que ponte en situación, ya has salido de la tierra, del mundo del Bloc de Notas, de Word, del Notepad Plus y de cualquier editor del universo que conoces; estás a punto de aterrizar en Vim. Recuerda que esto es otro planeta, aquí no hay barras de menú, ni botones con iconos de colores, ni siquiera deberías usar el ratón, ni los cursores. Todo parece desierto, como en la luna, todo está bajo la superficie, justo bajo las yemas de tus dedos.

Abre el editor, para ello invoca a vim desde la línea de comandos cargando el fichero de ejemplo `vim primeras_ordenes.txt` o abre el fichero desde una versión gráfica de vim.

Si lo has hecho bien aparecerá el contenido del fichero, si algo ha fallado puede que estés viendo algo parecido a esto, no pasa nada, es la pantalla de créditos de vim.

![creditos_iniciales_vim](/Users/juananruiz/repos/curso-vim/img/creditos_iniciales_vim.png)

Utiliza las teclas `h, j, k, l` para moverte a izquierda, abajo, arriba y derecha del texto (un truco para no perderte es que la j parece una flecha hacia abajo)

Ve a la última línea del fichero usando la tecla `j`, cuando llegues a la línea en blanco pulsa `i`. Ahora puedes teclear texto como si estuvieras en un editor normal, escribe lo siguiente:
"A un panal de rica miel cien mil moscas acudieron..."

Cuando termines pulsa la tecla Escape (`ESC`) y estarás de vuelta al modo normal (normal para Vim, puede que todavía sea un poco raro para ti). Prueba ahora a borrar algunos caracteres usando la tecla `x` observa que puedes borrar pero no puedes escribir. Si quieres volver a escribir sitúate con  ayuda de las teclas  `h, j, k, l`  en donde quieras y entonces pulsa `i` . Observa que tras pulsarla puedes empezar a escribir delante de donde tenías el cursor (la i viene de insertar). 

Cuando te canses de practicar pulsa `ESC`, y entonces teclea: `:q`

 Este es el comando para salir de Vim sin guardar, si has hecho algún cambio se quejará de que no has guardado todo el trabajo que has hecho, como ahora no queremos guardar escribe entonces: `:q!`

Para recordar el signo de admiración recuerda que puedes sustituirlo mentalmente por cualquier imprecación que necesites soltar. Yo suelo pensar:
"¡Salte ya, repámpanos!"

Si quieres guardar el fruto de tu esfuerzo teclea `:wq` para guardar y salir.

Estas tres últimas ordenes que has utilizado son un tipo especial de ordenes a las que llamamos **modo comando**, se distinguen por los dos puntos y porque aparecen siempre en la línea inferior de la ventana.

## Tu chuleta de Vim

A lo largo del curso te iré dando algunas chuletas que te podrán ser de utilidad, y que quedarán muy chulas en tu escritorio, pero es muy importante confeccionar una propia. 

Coge papel y boli y en un rinconcito apunta estos primeros comandos que has aprendido y para que sirven cada uno de ellos, puedes ver en la ilustración una idea de como podría ser esta chuleta, pero no tiene porqué ser exactamente así. Al final del curso tendrás la hoja entera rellena 

![chuleta_manuscrita_fase1](chuletas/chuleta_manuscrita_fase1.jpeg)

## Resumen de comandos de esta etapa

Todavía no hemos hablado de los modos, pero los menciono aquí para que te vayas haciendo el oído, hablaremos de ellos en nuestra próxima etapa.

### Modo normal

`h` → mover cursor un carácter hacia la izquierda

`j` → mover cursor una línea hacia abajo

`k` → mover cursor una línea hacia arriba

`l` → mover cursor un carácter hacia la derecha



`i` → comenzar a escribir antes del cursor, entra en modo inserción

`x` → borrar el carácter bajo el cursor, no entra en modo inserción

`ESC` → volver a modo normal


### Modo comando

`:q` → salir de vim 

`:q!` → salir de vim forzado

`:wq` → salir de vim guardando antes

----

[<< Preparándote para el viaje](https://github.com/juananruiz/curso_vim/blob/master/temario/preparandote_para_el_viaje.md) - [Volver al índice](https://github.com/juananruiz/curso_vim) - [Comenzar a respirar >>](https://github.com/juananruiz/curso_vim/blob/master/temario/comenzar_a_respirar.md)
