# Las macros aumentan tus poderes 

En la mayoría de los editores de texto es fácil editar y muchísimo más complicado hacer macros, en Vim por fin, es al revés. Y esto así porque Vim es un lenguaje de edición y si conoces el lenguaje escribir un pequeño cuento es sencillo.

Prácticamente no necesitas aprender nada nuevo para hacer macros en Vim, solo tienes que aplicar lo que ya sabes y un par de trucos que te voy a contar.

Las macros en Vim se declaran escribiendo `q` y otra letra cualquiera en minúscula, esto te da 24 macros que podrías mantener en memoria, incluso, si no las sobreescribes, estarán ahí la próxima vez que arranques vim. 

Ten en cuenta que las macros se graban en los mismos registros que el "portapapeles" de vim, por lo que si declaras una macro en el registro **a** y luego copias algo en ese registro te cargas la macro. Es cuestión de organizarte, tienes 24 registros.

Te lo repito de nuevo, las macros se graban en registros, los fragmentos de texto que copias o cortas también se graban en el registro. Para el registro no hay diferencias entre macros y fragmentos de texto, si copias un fragmento de texto al registro ""a"" y luego tecleas `@a` Vim intentará ejecutar como una macro ese fragmento de texto. Si, por el contrario, grabas una macro en el registro ""b"" y luego tecleas `"bp` Vim copiará los comandos de tu macro a la derecha de la posición actual del cursor.

Y ahora te invito a crear una macro, y te pido que vayas siguiendo estos pasos conmigo.

### Un ejemplo de macro

Vas a hacer una macro para subrayar una línea de un título con guiones, pero el numero de guiones tiene que ser igual que el número de caracteres de la línea para que quede con la misma longitud. Con un editor de texto normal tendrías que teclear tantos guiones como caracteres y luego dar un masaje a la yema de tu dedo meñique, con vim lo haces con 6 pulsaciones: `yypVr-`

Como ya te estás vim-acostumbrando me dirás que si tienes que subrayar diez títulos que diez por seis son sesenta y que seguro que vim puede hacerlo mejor ¡faltaría más! 

Entonces haz lo siguiente, sitúate sobre la línea que vas a subrayar, da igual la posición. 

1. Teclea `qs` para empezar a grabar la macro en el registro **s** (s de subrayado para acordarte)

2. Teclea la secuencia de comandos que formarán la macro: `yypVr-`

3. Pulsa `q`

4. Tendrás tu título con un subrayado exacto.

5. Ve al siguiente título que tengas que subrayar y teclea `@s` ¡chan ta ta chan!

   

### Editar una macro

Supón que ya tienes una estupenda y laboriosa macro guardada en el registro **a** y necesitas hacer un pequeño, o gran, cambio a la macro para dejarla perfecta. Sigue estos pasos y tendrás un dominio absoluto sobre tus macros:

1. Escribe `:let @a='` (desde el modo comando evidentemente).
2. Pulsar `Ctrl-R Ctrl-R a ` para insertar el contenido actual del registro **a**.
3. Edita el texto como necesites.
4. Añade otra comilla simple (`'`) para cerrar y pulsa `ENTER`
5. Escribe `:reg a` para ver el nuevo valor del registro.
6. Teclea `@a` para ejecutar la macro.

### Almacenar la macro en tu fichero .vimrc

Las macros se quedan almacenadas en sus registros aunque reinicies vim o el ordenador, pero si estás haciendo un trabajo más largo igual te interesa almacenarla en tu fichero **.vimrc**.

Hacer esto es muy fácil, simplemente sigue los pasos que acabamos de ver en **Editar una macro** pero desde dentro de tu fichero **.vimrc** y sin poner los dos puntos delante de **let**.

Salva tu fichero **.vimrc** y a partir de ahora cada vez que inicies vim esa macro quedará asignada a ese registro. 
