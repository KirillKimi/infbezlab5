---
# Front matter
title: "Лабораторнаяработа № 5"
subtitle: "Дискреционное разграничение прав в Linux. Исследование влияния дополнительных атрибутов"
author: "Сидоракин Кирилл Вячеславович НБибд-01-18"

# Generic otions
lang: ru-RU
toc-title: "Содержание"

# Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

# Pdf output format
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
### Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Misc options
indent: true
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=070 # the penalty for breaking a line at a binary operator
  - \relpenalty=050 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=010 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
  - \usepackage{rotating}
  - \usepackage{tabularx}
---

# Цель работы

Изучение механизмов изменения идентификаторов, применения SetUID- и Sticky-битов. Получение практических навыков работы в консоли с дополнительными атрибутами. Рассмотрение работы механизма смены идентификатора процессов пользователей, а также влияние бита Sticky на запись и удаление файлов.

# Выполнение лабораторной работы

Создаем программу simpleid.c: 
![Создание файла](image/1.jpg){ #fig:001 width=50% }
![Создание файла](image/2.jpg){ #fig:001 width=50% }

Скомплилируем программу gcc simpleid.c -o simpleid
![Чтение и запись](image/3.jpg){ #fig:002 width=50% }

Выполняем программу simpleid: ./simpleid
![Выполнение команды](image/4.jpg){ #fig:003 width=50% }

Выполняем системную программу id: 
![Программа ID](image/5.jpg){ #fig:003 width=50% }

Усложняем программу, добавив вывод действительных идентификаторов:
![simpleid2.c](image/6.jpg){ #fig:004 width=50% }
![simpleid2.c](image/6.1.jpg){ #fig:004 width=50% }

Компилируем и запускаем simpleid2.c:
![simpleid2.c](image/7.jpg){ #fig:007 width=50% }

От имени суперпользователя выполняем команды:
![simpleid2.c](image/8.jpg){ #fig:007 width=50% }

Используем sudo
![sudo](image/9.jpg){ #fig:007 width=50% }

Выполняем проверку правильности установки новых атрибутов и смены владельца файла simpleid2
![ls](image/10.jpg){ #fig:007 width=50% }


Запускаем simpleid2 и id 
![simpleid2 и id](image/11.jpg){ #fig:007 width=50% }

Создаем программу readfile.c
![readfile.c](image/12.jpg){ #fig:007 width=50% }

Откомпилируем её
![readfile.c](image/13.jpg){ #fig:007 width=50% }

# Вывод

В результате выполнения лабораторной работы мы получили навыки изучения механизмов изменения идентификаторов, применения SetUID- и Sticky-битов. Получили практические навыки работы в консоли с дополнительными атрибутами. Рассмотрели работы механизма смены идентификатора процессов пользователей, а также влияние бита
Sticky на запись и удаление файлов.