
Primeros pasos - Curso básico de VIM - Universidad de Sevilla
=============================================================

Vamos a empezar con el mínimo equipo necesario para sobrevivir al primer encuentro con vim.

A quien nunca lo haya manejado le recomiendo entrar primero por su cuenta en un fichero de pruebas e intentar hacer algo. Será frustante ahora, pero más adelante recordarás este primer momento con cariño.

Bueno cuando estés a punto de gritar pulsa la tecla ESCAPE (ESC a partir de ahora) y luego :q! 

Ahora volvemos a entrar de nuevo pero con conocimiento de causa.

----------------------------------------------------------------------------------------------------------------------------------
### Concepto 1: Vim es un editor basado en modos, el modo por defecto se llama modo NORMAL, no sirve para escribir (ya lo entenderás). 

1. Pulsa i para entrar en modo INSERT.

2. Ahora puedes escribir como en cualquier otro editor, algún día este modo te parecerá el más aburrido.

3. Prueba a escribir algo, a borrar, etc. En algunos entornos puede que no funcionen los cursores o la tecla de borrar hacia atrás. No te preocupes demasiado por ello. Vim es un editor acostumbrado a las condiciones más duras, trabajando en cualquier sistema operativo y con los terminales más arcaicos que existe pero sabe salir airoso de todos estos problemas.

4. Cuando te canses de escribir pulsa ESC para salir del modo INSERT y volver al NORMAL

------------------------------------------------------------------------------------------------------------------------
Concepto 2: En modo NORMAL las teclas sirven para otras cosas, este es el modo más potente y productivo, la joya de Vim.
------------------------------------------------------------------------------------------------------------------------

1. Prueba ahora a moverte por el texto usando los "cursores" de vim: hjkl (izquierda, abajo, arriba, derecha), lo bueno de habituarte a ellos es que podrás usarlos en cualquier entorno (aunque no funcionen los cursores) y te ayudarán a dejar el vicio de usar los cursores.

2. Muévete un poco por el texto y cuando veas un caracter que te de coraje pulsa x para borrarlo. 

3. Si quieres borrar una línea entera pulsa dd. Y si quieres pegarla en otro lado muevete con j o k y pulsa p para pegar.

4. Práctica un poco con estos pocos comandos y cuando te canses utiliza ESC + :q! para salir sin grabar o ESC + :wq para salir grabando

5. Habrás observado que cuando tecleas ESC + : el cursor baja a la línea inferior (se llama linea de comandos) y se muestran los dos puntos, has pasado a un nuevo modo, el modo COMANDO.
