# Personalizando Vim: el fichero vimrc

Para configurar Vim, como no podía ser menos, se utiliza un fichero de texto perfectamente legible y editable, el fichero .vimrc.

Este fichero normalmente lo puedes encontrar en:

1. Configuración general de vim para todo el sistema
2. Tu directorio raiz de usuario como fichero oculto: .vimrc
3. Tu directorio raiz, dentro del directorio oculto .vim

Aquí tienes un fichero de configuración bastante completo

```shell
"
" Alunizando con Vim
" Un buen comienzo para tu fichero .vimrc
"

" Quieres Vim, no vi. Cuando Vim encuentra un fichero .vimrc se pone por defecto en modo 'nocompatible'. En cualquier caso así queda claro cuales son tus intenciones ;-)
set nocompatible

filetype plugin indent on  " Habilita la carga del plugin adecuado para el resaltado de sintáxis de cualquier tipo de fichero y su indentación correcta
syntax on                  " Habilita resaltado y coloreado de sintáxis (en función del tipo de fichero: php, conf, js, etc)

set autoindent             " Indenta la siguiente línea automáticamente en función de la anterior
set expandtab              " Utiliza espacios en lugar de tabuladores
set softtabstop =4         " Cada tabulador equivale a 4 espacios
set shiftwidth  =4         " Los reindentados automáticos serán de 4 espacios
set shiftround             " Los reindentados automáticos serán múltiplos de lo que digas en shiftwidth

set hidden                 " Permite cambiar de buffer sin tener que guardar antes
set laststatus  =2         " Muestra la línea de estado
set showmode               " Muestra el modo actual en la línea de estado
set showcmd                " Muestra las teclas que vamos pulsando en modo comando
set statusline=%<%f%h%m%r%=%b\ 0x%B\ \ %l,%c%V\ %P

set incsearch              " Va buscando a medida que vayamos tecleando en modo / o ?
set hlsearch               " Resalta las búsquedas
set ignorecase             " Insensible a minusculas/mayusculas en las busquedas

set ttyfast                " Acelera el refresco de pantalla
set lazyredraw             " Sólo refresca la pantalla cuando es necesario

set splitbelow             " Abre nuevas ventanas debajo de la actual
set splitright             " Abre nuevas ventanas a la derecha de la actual

set number                  "Numerado de líneas
set relativenumber          "Numeración relativa
set cursorline             " subraya la línea actual para que sepamos por donde vamos
colorscheme blue "default blue darkblue slate default delek desert elflord evening koehler morning murphy pablo peachpuff ron shine slate torte zellner

"Pasando de backups
set nobackup
set nowb
set noswapfile

" Opciones para un vim más ortodoxo
set guioptions-=m "quita la barra de menu en modo gráfico
set guioptions-=T "quita la barra de herramientas en modo gráfico
nnoremap <up> <nop>
nnoremap <down> <nop>
nnoremap <left> <nop>
nnoremap <right> <nop>
inoremap <up> <nop>
inoremap <down> <nop>
inoremap <left> <nop>
inoremap <right> <nop>

" Truco de regalo: permite salvar ficheros como sudo cuando se te olvide hacer sudo vim
cmap w!! w !sudo tee > /dev/null %

" Abreviaturas
iabbrev jarr Juan Antonio Ruiz Rivas  
iabbrev usev Universidad de Sevilla
```
