# Vista de rayos X para búsquedas y sustituciones

### Búsqueda rápida

Una forma rápida de buscar la siguiente aparición de la palabra en la que tienes el cursor es pulsar `*` luego con `n` o pulsando de nuevo `*` puedes buscar la siguiente. Si quieres la aparición anterior pulsa `#`. Estos dos comandos buscan palabras exactas, no fragmentos de cadena. 

### Búsqueda con / y ?

Ya sabes que para buscar cualquier cadena en un fichero sólo tienes que pulsar `/` en modo normal, después tecleas la cadena que quieres buscar y pulsas `<ENTER>` para que el cursor salte a la siguiente aparición de esa cadena. 

Si ahora pulsas la tecla `n` irás a la siguiente aparición de la cadena que buscas, cuando llegues al final del fichero te dará un aviso y volverá a buscar desde el principio. Si quieres ir a la aparición anterior teclea `N`

En realidad el modo búsqueda funciona con expresiones regulares como puede que aún no las conozcas sólo te  daré algunos trucos aquí. 

- Algunos caracteres no se pueden usar directamente `^`,`.`, `$` o `\` porque tienen un significado especial.
- Si quieres buscar una palabra exacta (p.e "pero") utiliza `/\<pero\>` . Esto encuentra "pero", pero no "ropero" o "perorata". A mi esta construcción siempre se me olvida, así que uso un truco para recordarla, me voy a cualquier palabra del texto en modo normal (¿en que modo estabas si no?) y pulso `*` entonces Vim, en la línea inferior me pinta la búsqueda exacta que acaba de hacer.
- Siguiendo con el ejemplo anterior `/pero\>` te devuelve "pero" y "ropero". Mientras que `/\<pero` te devuelve "pero" y "perorata".


### Sustituciones

### El modo visual

Algo muy interesante del modo visual es que en el siguen funcionando todos los comandos de movimiento, así que puedes entrar en modo visual y teclear t. para seleccionar hasta el próximo punto. Por supuesto también sirven $, 0, w, }, etc para seleccionar hasta el final de la línea, hasta el principio, una palabra, un párrafo, etc.

### Los registros

En Vim el concepto de portapapeles de otras aplicaciones se maneja con algo mucho más versátil: los registros.

Cada vez que copias algo en vim lo puedes hacer en un total de 24 registros distintos, las 24 letras del alfabeto. Luego puedes "pegar" o hacer otras operaciones utilizando cualquiera de estos 24 registros.

Para copiar la línea actual al registro **a** teclea `"ayy` , a continuación puedes pegar con `"ap`

Además de las 24 letras a tu disposición hay una serie de registros por defecto: 

* `"*` → portapapeles del sistema
* `""` → registro sin nombre, es al que se copia aquello que borres
* `"0` → registro cero, es al que se copia aquello que copies
