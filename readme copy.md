Библиотека atomic css разделена на три части.
1. atomic_main.css - основные стили.
2. atomic_M1.css, atomic_M2.css, atomic_M3.css - основные стили для Media queries.
2. atomic_custom.css - стили и Media queries стилей, характерные для данного проекта - палитра цветов, палитра размеров, палитра позиционирования, стили для focuc, hover и active. Сюда же вынесены общие классы типа .container и переменные (кастомные свойства).

================================== 

Общие правила нейминга:

1. css-свойства, параметры и значения разделяются символом "_" 

.pos_rel {position: relative;}

2. css-свойства, параметры и значения, записанные через дефис, так же пишутся через дефис с сокращениями

.l-h_22 {line-height: 22px;}
.trs-p_b-sh  {transition-property: box-shadow;}

3. некоторые части длинных названий css-свойств и их значений пропускаются для удобства и сокращения записи:

.j-c_between {justify-content: space-between;}
.trs-f_e {transition-timing-function: ease;}

================================= 

Частные правила:

1. псевдоэлементы и состояния hover, focuse и active вынесены вперед для удобства восприятия в коде, состояния записаны впереди псевдоэлементов (это позволяет наглядно отделять свойства элемента от свойств его псевдоэлементов и их состояний) :

.bef_pos_rel::before {position: relative;}
.act_c_violet-200:active {color: var(--c_violet-200);}
.act_bef_b-c_violet-700:active::before {background-color: var(--c_violet-700);}

2. некоторые свойства не совсем атомизмрованы, но очень удобны в применении:

.brd_1 {border: 1px solid transparent;}

3. для transition с несколькими параметрами сделаны отдельные классы - для каждого набора свой класс (в связи с особенностями этого свойства его нельза полностью атомизмровать):

.trs-p_c_brd_op_h  {transition-property: color, border, opacity, height;}

===================================== 

Media queries

Брекпоинты не привязаны к конкретным значениям и обозначены как M1, M2, M3 и т.д. в отличии от многих других библиотек.
Это дает гибкость настроек под конкретный проект - можно устанавливать и бысто менять  конкретные значения media queries и их количество. Так же это легко позволяет использовать Mobile First или Desktop First подходы (в отличии от Bootstrap).
В исходной библиотеке media queries представляют собой отдельные файлы css для каждого брекпоинта atomic_M1.css, atomic_M2.css и т.д. Каждый файл представляет по сути копию основного atomic.css в соответствующем media querie и добавлением каждому классу литеры M1, M2, M3. При завершении верстки проекта эти файлы можно объединить в один, где будут находиься только использованные классы, а не использованны удалить.

=====================================

Сокращения.

tp  top
rg  right
bt  bottom
lf  left

box-sz    box-sizing
pos       position
z         z-index
d         display
a-it      align-items
j-c       justify-content
fl-dir    flex-direction
fl-wr     flex-wrap
a-con     align-content
j-s       justify-self
fl-shr    flex-shrink
fl-grw    flex-grow

w     width:
h     height
m     margin
p     padding

f-f   font-family
f-w   font-weight
f-st  font-style
f-sz  font-size
l-h   line-height
t-al  text-align

c        color
brd      border
brd-rad  border-radius
brd-c    border-color
b-c      background-color
b-pos    background-position
b-cl     background-clip
b-rep    background-repeat
b-sz     background-size

cr_point {cursor

pnt-ev_none {pointer-events

o-fit_cont {object-fit

o-pos_center {object-position

out_none {outline

over_hidden {overflow:

op_0 {opacity:

v-hid {visibility:

trs-d_100 {transition-duration

trs-f_e {transition-timing-function

trs-p_all  {transition-property

bef_cont::before

aft_cont::after

foc_c_violet-200:focus

act_c_violet-200:active

is-act_aft_trf_r_-45_trltY_4.is-active

hov_c_main-light:hover
