# Primera notas Evernote

Mi fuente principal de inspiración:
http://yannesposito.com/Scratch/en/blog/Learn-Vim-Progressively/

https://youtu.be/_NUO4JEtkDw 

https://www.udemy.com/vim-commands-cheat-sheet/
Tutoriales Linux, Vim, etc Santiago Romero
Editor Vim
https://github.com/mhinz/vim-galore
http://www.oualline.com/vim-cook.html - Recetario de VIM
http://www.moolenaar.net/habits.html - Seven habits of effective text editing  
http://wiki.us.es/juanan/wakka.php?wakka=EditorVim
https://www.ibm.com/developerworks/linux/tutorials/l-vi/index.html
https://www.reddit.com/r/vim/

Descargar Vim para cualquier sistema operativo
https://vim.sourceforge.io/download.php
Primero: Duele
Segundo: Engancha
Tercero: Modo Dios

----

Por algo lo llaman "Normal Mode": vim es un editor enfocado a la edición de texto, no a la escritura del mismo. ¿Entonces no sirve para escribir? Si, también, pero es que, al fin y al cabo pasamos mucho más tiempo editando que escribiendo, sobre todo si hablamos de programación, ficheros de configuración, datos en bruto, etc.

Al principio quizás te hagas un lío porque no recuerda en que modo se encuentra cuando está en Vim, parece un fastidio eso de tener que teclear "i" o "a" cada vez que se quiere escribir algo. Y si empiezan a escribir estando en modo Normal de pronto empiezan a ejecutar comando que lo lían todo. Por ejemplo abre un documento de texto, uno bien llenito, y escribe, como sin querer, dG, de pronto has borrado todo el texto. "Aggg, ¿cómo es posible que alguien use este editor?", no pasa nada, pulsas la "u" y todo vuelve a estar igual. Como acabo de contaros vim está pensado para editar, pero no para editar y punto, para editar a la velocidad del rayo, de manera inteligente, evitando muchísimos errores y ahorrando muchiiiiiiiiiiiiiiiiisimas pulsaciones de teclado, o viajes del teclado al ratón y vuelta. En el ejemplo anterior la "d" le dice a Vim que vas a borrar algo y la "G" nos traslada al final del documento, con lo que se borra todo el documento. La "u" deshace la última acción que hayamos realizado, así que quizás sea lo primero que debas aprender.

----

A un panal de rica miel diez mil moscas acudieron que por golosas murieron presas de patas en él.

Cuentan de un sabio que un dia, tan pobre y misero estaba, que solo se alimentaba de las hierbas que cogía. "Habrá -para si decía- alguien más pobre que yo", y la respuesta encontró cuando al volver la cabeza vio a otro sabio recogiendo las hierbas que el desechó. 


You cannot use Vi properly before knowing at least a handful of commands. This makes the threshold rather high. Vi doesn't get fast before you know 25 commands or so, and you won't be the cool dude(tte) before you know even more. Note that this is also true for Emacs. However, Emacs is much easier to use as a newbie.

Más trucos
Dedos cruzados
Es habitual que al teclear rápido cambiemos una letra por otra. Por ejemplo: "Widnows". En vim esto se soluciona fácil usando la combinación "xp", ve a la primera letra mal colocada, la "d" y teclea "xp" con esto tendrás "Windows" sin haber salido del modo normal. El comando "x" borra la "d", el cursor avanza hasta la "n", el comando "p" pega de nuevo la "x", pero ahora detrás de la "n" ("P" pegaría delante)

Subrayar un título
Copias la línea de título con: yyp
Sustituyes con guiones con: v$r-

Deberes
primer día: hacer el tutorial de vim al menos hasta la lección 3 incluida
segundo día: de la 4 en adelante


Vim no tiene nada que ver con ningún editor de texto que hayas conocido antes.

Olvídate del ratón 

Siempre hay una manera mejor de hacer las cosas, no dejes de aprender    

Aprende algo nuevo cada semana

Tu nuevo amigo ~/.vimrc

Vim es un lenguaje, un lenguaje para editar
ciw - Change Inside Word
caw - Change A Word
ci) - Change Inside )
ca) - Change A ()

Otro modificador interesante es la t, pero no funciona con objetos de texto sino con carácteres
ctx - Change To x (desde la posición actual hasta la primera x


El esquema suele ser: comando + objeto de texto o movimiento

Comandos
d - delete            
c - change 
r - replace
v - selecciona 
y - copy
f - find  

Objetos de texto (se usan con i o a delante)
w - word  
s - frase (hasta el punto) (tiene que ser usados con i o a delante)
p - párrafo (hasta una línea en blanco) (tiene que ser usados con i o a delante)lock 
" - texto entre comillas dobles
t - bloque html (<h1>Mi web</h1>)
> - etiqueta html
>   *Q_to*        Text objects (only in Visual mode or after an operator)

|v_aw|       N  aw    Select "a word"
|v_iw|       N  iw    Select "inner word"
|v_aW|       N  aW    Select "a |WORD|"
|v_iW|       N  iW    Select "inner |WORD|"
|v_as|       N  as    Select "a sentence"
|v_is|       N  is    Select "inner sentence"
|v_ap|       N  ap    Select "a paragraph"
|v_ip|       N  ip    Select "inner paragraph"
|v_ab|       N  ab    Select "a block" (from "[(" to "])")
|v_ib|       N  ib    Select "inner block" (from "[(" to "])")
|v_aB|       N  aB    Select "a Block" (from "[{" to "]}")
|v_iB|       N  iB    Select "inner Block" (from "[{" to "]}")
|v_a>|       N  a>    Select "a <> block"
|v_i>|       N  i>    Select "inner <> block"
|v_at|       N  at    Select "a tag block" (from <aaa> to </aaa>)
|v_it|       N  it    Select "inner tag block" (from <aaa> to </aaa>)
|v_a'|       N  a'    Select "a single quoted string"
|v_i'|       N  i'    Select "inner single quoted string"
|v_aquote| N  a"    Select "a double quoted string"
|v_iquote| N  i"    Select "inner double quoted string"
|v_a`|       N  a`    Select "a backward quoted string"
|v_i`|       N  i`    Select "inner backward quoted string"

https://blog.carbonfive.com/2011/10/17/vim-text-objects-the-definitive-guide/

Para movimiento (también funcionan como objetos de texto, pero cuidadín)
b - word (backward)       
e - end word
} - final párrafo
$ - final línea
{ - principio párrafo
0 - principio línea

Vim funciona con mejor precisión cuando se usan objetos de texto para la edición, también se pueden
usar los comandos de movimiento para editar pero a la larga seremos más lentos y nuestras acciones menos 
intuitivas. Por ejemplo si me equivoco tecleando una palabra es mejor borrar la palabra entera y volver a escribirla
que moverse hasta el error para borrar y reescribir desde allí

%  - te lleva de un paréntesis que abre a otro que cierra y viceversa, también funciona con llaves y corchetes

x - borra un sólo carácter (y no se sale de modo normal)

dd borra párrafo entero

Pista 1 - algunos comandos hacen algo y siguen en modo normal, otros te pasan a modo insertar 
Ejemplos
x - borra un caracter y sigue en modo normal
o - inserta un nuevo párrafo y entra en modo insertar
c - borra algo y entra en modo insertar
d - borra algo y sigue en modo normal


Búsqueda por caracter
f - busca hacia delante
F - busca hacia detrás
t - busca pero se queda en el carácter anterior
T - lo mismo pero hacia atrás
; - repite la búsqueda hacia delante
, - repite la búsqueda hacia atrás

Pista X: los comandos en minúscula hacen "algo" hacia adelante, los comandos en mayúsculas hacen "algo" hacia atrás. 

Ejemplos
fg - busca la letra g
5f, - busca la quinta coma
t= - busca un igual pero se queda delante


Más "difícil" todavía 
5dw - delete 5 words
6rx - reemplaza 6 caracteres por la letra "x"
10dd - borra 10 líneas

Lo mismo vale para los movimientos
5j - 10 líneas abajo
4w - 4 words adelante

G - va al final del fichero
gg - va al principio del fichero 
33gg - va a la línea 33 (también vale con 33G)


Objetos de texto
w: principio de palabra adelante(word)
e: final de palabra (end)
b: principio de palabra anterior

Mi gato no come
w-->     

{: principio de párrafo
}: final de párrafo 

La ayuda de vim es un gran recurso para aprender y mejorar, pero nadie te cuenta un par de trucos imprescindibles para llevarse bien con ella.

Lo básico
:help o :h para acceder a ella
:h <tema concreto o comando>  ejemplo ":h  grep" o ": h ."

Lo que nadie te cuenta
Usa :bd para salir de la ayuda sin cerrar el resto de buffers (documentos)
Usa CTRL-W + [h,j,k o l] para moverte entre la ventana de la ayuda y la ventana donde estás trabajando

Practicando:
Teclea :h / para acceder a la ayuda  búsquedas en vim
Lo normal es que la ayuda se abra encima de la ventana actual y el cursor se sitúe allí


Guía de supervivencia para VIM

i    Pasar a modo insert (empezar a escribir)
ESC  Volver a modo normal
:q   Salir (quit)
:w   Escribir (write)
:q!  Salir sin grabar cambios

h    Mueve el cursor un carácter hacia la izquierda
j    Mueve el cursor una línea hacia abajo
k    Mueve el cursor una línea hacia arriba
l     moves the cursor one character to the right.
0    moves the cursor to the beginning of the line.
$    moves the cursor to the end of the line.
G   move to the end of the file.
gg move to the beginning of the file.
`. move to the last edit.

dd borra la linea entera.
dw will delete a word.
u will undo the last operation.
Ctrl-r will redo the last undo.

Ejemplos de .vimrc
https://github.com/thoughtbot/dotfiles/blob/master/vimrc
https://github.com/juananruiz/dotfiles/blob/master/.vimrc

.vimrc mínimo
set backspace=2         " backspace in insert mode works like normal editor
syntax on               " syntax highlighting
filetype indent on      " activates indenting for files
set autoindent          " auto indenting
set number              " line numbers
colorscheme desert      " colorscheme desert
set nobackup            " get rid of anoying ~file