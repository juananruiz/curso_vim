# Comenzar a respirar
Si has llegado hasta aquí lo has conseguido, has sobrevivido al primer impacto, pero no te confíes, sigues en un ambiente hostil. Tienes que aprender a respirar de nuevo, a moverte de nuevo, casi que a pensar de nuevo, ya te dije que Vim era diferente.

## Los modos de Vim

Una de las características más distintivas de Vim es que es un editor basado en *modos*, dependiendo del modo en que te encuentres Vim se comportará de forma diferente. 

### El modo normal

Cuando accedes a Vim, entras en Modo Normal, se llama así porque es el modo en que deberíamos esta casi todo el tiempo. En el planeta de donde vienes se llama editores de texto a unos programas que sirven para teclear texto, borrar un poco, volver a teclear, etc. Deberían llamarse "escritores de texto", Vim por el contrario es un auténtico "editor de texto", sabemos que es así porque en modo Normal, sólo se puede editar, para escribir hay que pasar a otro modo que se llama Modo Insertar. 

Esta diferencia es la que hace que al principio te explote la cabeza cuando te enfrentas a Vim, todo el mundo te dice que es un editor de texto, tu vienes de un mundo en que un editor de texto es otra cosa, y cuando intentas escribir en Vim no se comporta como esperabas. Pero bueno, has venido aquí por los superpoderes, y los vas a tener, sigamos.

### El modo Insertar

En Modo Insertar Vim se parece bastante a lo que tu conoces, tú tecleas y él escribe las letras que has pulsado. Debes acostumbrarte a pasar poco tiempo en este modo. La rutina normal sería:

1. Buscas en que parte del texto quieres trabajar
2. Te mueves hasta esa parte usando los comandos de desplazamiento de Vim
3. Tecleas un poco, pulsas ESC y buscas de nuevo donde tienes que seguir trabajando. O pulsas ESC, te mueves a otro sitio y repites la misma acción que acabas de hacer pulsando sólo una o dos teclas.

### El modo Visual

Un tercer modo muy potente es el Modo Visual, en este modo seleccionas un punto de partida y un punto final en el texto para trabajar con él. Puedes usar los comandos de desplazamiento y los objetos de texto para ampliar o acortar tu selección. Una variante del Modo Visual es el Modo Bloque Visual, parecido al anterior pero trabaja con columnas en vez de con líneas, este modo te permitirá hacer maravillas con datos tabulados.

### Cambiando de modo

Incluso cuando estés escribiendo de corrida un texto más largo, deberías acostumbrarte a pulsar ESC en las pausas naturales del texto. Esto te permitirá hacer y deshacer más fácil, repetir discrecionalmente las acciones que hayas hecho y te da un pequeño respiro antes de seguir tecleando para que veas como va quedando tu obra maestra.

Al principio quizás te hagas un lío porque no recuerdas en que modo te encuentras cuando estás en Vim. Parece un fastidio eso de tener que teclear "i" o "a" cada vez que se quiere escribir algo. Y si empiezas a escribir estando en modo Normal de pronto empiezas a ejecutar comando que lo lían todo. Por ejemplo abre un documento de texto, uno bien llenito, y escribe, como sin querer: `dG` de pronto has borrado todo el texto. 

"¡Aggg! ¿cómo es posible que alguien use este editor?", no pasa nada, pulsas la `u` y todo vuelve a estar igual. Como acabo de contarte Vim está pensado para editar, pero no para editar y punto, para editar a la velocidad del rayo, de manera inteligente, evitando muchísimos errores y ahorrando muchísimas pulsaciones de teclado, o viajes del teclado al ratón y vuelta. En el ejemplo anterior la `d` le dice a Vim que vas a borrar algo y la `G` nos traslada al final del documento, con lo que se borra todo el documento. La `u` deshace la última acción que hayamos realizado, así que quizás sea lo primero que debas aprender: u de "undo", deshacer. Y ya de paso, si te pasas al deshacer pulsa `CTRL-r` para rehacer.

En la etapa anterior aprendiste a usar en modo inserción utilizando la `i` pero hay muchas maneras de entrar al modo inserción, cada una aporta algo distinto, claro:

`a` → Insertar después del cursor

`o` → Insertar una línea bajo la actual 

`O` → Insertar una línea sobre la actual 

`I` → Insertar al principio de la línea actual

`A` → Insertar al final de la línea actual

Como ves muchos comandos de Vim hacen cosas parecidas cuando están en minúsculas o mayúsculas:
`a` / `A`
 `i` / `I`
 `o` / `O` etc...

Veamos algo más potente, estando en modo normal, colócate al principio de alguna palabra que te caiga mal y pulsa `cw`. Con esto has borrado una palabra y entras en modo inserción. Esto parece poca cosa pero ya verás las posibilidades que encierra.

Sigamos con algunos movimientos: 

#### Movimientos básicos

`0` → (cero) ve a la primera columna
`^` → ve al primer carácter 'visible' de la línea actual
`$` → ve al final de la línea
`g_` → ve al último carácter visible de la línea (nunca lo he usado)
`CTRL-B` → una pantalla hacia arriba
`CTRL-F` → una pantalla hacia abajo
`/patito` → busca "patito"

#### Copiar y pegar

`P` → pegar delante, recuerda que `p` es pegar a continuación.
`yy` → copia la línea actual, es un atajo de `ddP` (que a su vez es un atajo de `d$P`)

#### Deshacer y rehacer

`u` → deshacer
`<C-r>` → rehacer

Frente a otros editores de texto que deshacen los cambios carácter a carácter la `u` de Vim 'recuerda' las acciones de Vim de manera combinada por lo que el deshacer es mucho más natural y fiable, esto se eleva a la máxima potencia cuando te acostumbres a usar Vim 'a la manera de Vim'

#### Abrir/Grabar/Salir/Cambiar de fichero (buffer)

`:e <ruta/archivo>` → abre archivo
`:w` → graba el archivo actual
`:saveas <nueva_ruta/nuevo_archivo>` → graba el archivo actual con otro nombre y/o ruta y ábrelo para editar
`:x`, `ZZ` or `:wq` → save and quit (`:x` only save if necessary)
`:q!` → quit without saving, also: `:qa!` to quit even if there are modified hidden buffers.
`:bn` (resp. `:bp`) → show next (resp. previous) file (buffer)


## Tómate un respiro

Comprendo que todo esto que estamos viendo te resulte un poco apabullante. Son demasiados modos, demasiados comandos, verbos, objetos, etc. Es normal, todos los que flipamos con Vim hemos pasado por eso. No te preocupes, a medida que vayas usando Vim un poco más y que vayas pillando su filosofía empezarás a interiorizar todo esto. Y entonces trabajaras de Vim de forma natural, y procesarás archivos a una velocidad endiablada. 

Mientras tanto respira, no te agobies, toma tu tiempo y dedica un rato a manejar y mejorar en Vim cada vez que tengas oportunidad. Si tienes que editar algún fichero, piensa, ¿podría hacerlo con Vim?
