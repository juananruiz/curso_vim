# Vuela como si no te afectara la gravedad

En la anterior etapa has superado el pánico inicial, incluso puede que te sientes cómodo. Es hora de orientarse y tomar el mando de esta misión.

> Si has cerrado y abierto de nuevo Vim puedes saber en que zona del planeta has caído utilizando el comando :pwd (igual que si estuvieras en Linux, pero con los dos puntos delante), con esto sabrás en que directorio del disco te encuentras. Mira ahora la barra inferior, justo encima de la línea de comandos, ahí tienes más información....
>

En un editor terrestre tienes que ir paso a paso, para moverte, para editar, para todo. Aquí puedes aprovechar la menor gravedad y empezar a moverte dando saltos más grandes. En este sentido Vim te ofrece algo único: un lenguaje de edición. Este lenguaje tiene sus verbos, sus objetos e incluso sus adverbios (modificadores).

Prueba ahora esto: estando en modo normal, colócate al principio de alguna palabra que te caiga mal y pulsa `cw`. Con esto has borrado una palabra y entras en modo inserción. Puedes reemplazar ahora la palabra por otra que te guste más. Pulsa `ESC` para volver a modo normal cuando termines. Esto parece poca cosa pero ya verás las posibilidades que encierra.

#### Verbos sin objeto

Estos verbos hacen lo que hacen y no se pueden combinar con objetos, se comportan más bien como comandos.

`x` → borra el carácter después del cursor
`D` → borra desde el cursor hasta el final de la línea 
`C` → borra desde el cursor hasta el final de la línea y entra en modo inserción
`r` → reemplaza un carácter
`J` → une dos líneas 

#### Verbos con objetos

`d` → borra "algo"
`c` → borra "algo" y entra en modo inserción (change)

`y` → copia "algo" al portapapeles 

#### Modificadores de objetos

`-a-` → Uno, una → Comprende el objeto completo (incluyendo delimitadores)
`-i-` → En (inside, dentro) → Comprende el objeto (sin incluir delimitadores)

#### Objetos de texto 

`w` → palabra (word) Trata las palabras-separadas-por-guiones (o por puntos o por barras) como palabras distintas.
`W` → gran palabra (big Word) Trata las palabras-separadas-por-guiones como una sola palabra.
`ap` → un párrafo (si, si, la "p" que usamos para "pegar" aquí significa párrafo)
`as` → una frase (misma cosa que con la "p")
`a"` → texto entre comillas (incluye las comillas)
`a)` → texto entre paréntesis (incluye los paréntesis)
`ip` → dentro de un párrafo (no incluye el espacio en blanco)
`i)` → texto entre paréntesis (sin los paréntesis)

### Veamos, y practiquemos, algunos ejemplos

`daw` → borra una palabra
`yi}` → copia el texto entre corchetes (muy útil para copiar todo el código de una función)
`v/pepe` → selecciona desde la aparición del cursor hasta la aparición de la cadena "pepe".


Ahora te propongo que hagas el ejercicio que aparece en el fichero "copiando_funciones.php". Inténtalo primero por tu cuenta, luego sal sin grabar e inténtalo de nuevo con las instrucciones que aparecen abajo del todo del fichero.


> #### No te confundas
>
> El uso de  `t` en algunos comandos parece un modificador de objeto pero no lo es. En realidad es una orden de movimiento que le dice a Vim: "ejecuta el verbo que he puesto antes hasta que encuentres el carácter que voy a poner ahora"
>
> `vtw` → No selecciona una palabra sino que selecciona desde la posición actual del cursor hasta el siguiente carácter "w" en la línea actual 



Bien, utiliza estos comandos hasta sentirte cómodo con ellos, una vez que lo hayas hecho te sentirás prácticamente de nuevo como en casa, tomate tu tiempo. Podrás hacer con Vim lo que hasta ahora hacías con un editor normal, recuerda, tienes que adaptarte a tus nuevos superpoderes y el primer paso es poder hacer de nuevo tus acciones cotidianas. Puede que todavía te sientas un poco incomodo, pero sigue conmigo a la siguiente etapa de este alunizaje.

![Chuleta manuscrita fase 2](https://github.com/juananruiz/curso_vim/blob/master/chuletas/chuleta_manuscrita_fase2.jpeg)

[<< Comenzar a respirar](https://github.com/juananruiz/curso_vim/blob/master/temario/comenzar_a_respirar.md) - [Volver al índice](https://github.com/juananruiz/curso_vim) - [Muevete a la velocidad de la luz >>](https://github.com/juananruiz/curso_vim/blob/master/temario/muevete_a_la_velocidad_de_la_luz.md)
