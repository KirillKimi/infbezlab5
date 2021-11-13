---
## Front matter
lang: ru-RU
title: Лабораторная работа №5
author: |
	Сидоракин
institute: |
	 RUDN University, Moscow, Russian Federation
date: Ноябрь, 2021 Москва

## Formatting
toc: false
slide_level: 2
theme: metropolis
sansfont: NotoMono-Regular
header-includes: 
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true
---
## Цель лабораторной работы

Получение практических навыков работы в консоли с расширенными атрибутами файлов


## Создаем программу simpleid.c:
![Создание файла](image/1.jpg){ #fig:001 width=50% }


## Скомплилируем программу gcc simpleid.c -o simpleid
![Чтение и запись](image/3.jpg){ #fig:002 width=50% }

## Выполняем программу simpleid: ./simpleid
![Выполнение команды](image/4.jpg){ #fig:003 width=50% }

## Выполняем системную программу id: 
![Программа ID](image/5.jpg){ #fig:003 width=50% }

## Усложняем программу, добавив вывод действительных идентификаторов:
![simpleid2.c](image/6.jpg){ #fig:004 width=50% }

## Компилируем и запускаем simpleid2.c:
![simpleid2.c](image/7.jpg){ #fig:007 width=50% }

## От имени суперпользователя выполняем команды:
![simpleid2.c](image/8.jpg){ #fig:007 width=50% }

## Используем sudo
![sudo](image/9.jpg){ #fig:007 width=50% }

## Выполняем проверку правильности установки новых атрибутов файла simpleid2
![ls](image/10.jpg){ #fig:007 width=50% }

## Запускаем simpleid2 и id 
![simpleid2 и id](image/11.jpg){ #fig:007 width=50% }

## Создаем программу readfile.c
![readfile.c](image/12.jpg){ #fig:007 width=50% }

## Откомпилируем её
![readfile.c](image/13.jpg){ #fig:007 width=50% }





## Вывод
В результате выполнения лабораторной работы мы получили навыки изучения механизмов изменения идентификаторов, применения SetUID- и Sticky-битов. 
Получили практические навыки работы в консоли с дополнительными атрибутами. 
Рассмотрели работы механизма смены идентификатора процессов пользователей, а также влияние бита Sticky на запись и удаление файлов.