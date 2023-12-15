---
## Front matter
title: "Отчёт по лабораторной работе 5"
subtitle: "Архитектура компьютера"
author: "Абдурахмонова Рухшона Бахтиёровна"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
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
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Целью работы является приобретение практических навыков работы в Midnight Commander. 
Освоение инструкций языка ассемблера mov и int.

# Выполнение лабораторной работы

Открыла Midnight Commander, с помощью клавишь со стрелками и Enter перехожу в каталог ~/work/arch-pc.
Далее нажимаю F7 и создаю каталог lab05

![Запуск Midnight Commander](image/01.png){ #fig:001 width=70%, height=70% }

При помощи touch создала файл lab05-1.asm

![Создание файла lab05-1.asm](image/02.png){ #fig:002 width=70%, height=70% }

Открыла файл на редактирование клавишей F4, выбрала редактор mceditor, 
написала код программы из задания.

![Программа в файле lab05-1.asm](image/03.png){ #fig:002 width=70%, height=70% }

Открыла файл на просмотр клавишей F3 и проверила, что он содержит набранный код.

![Просмотр файла lab05-1.asm](image/04.png){ #fig:004 width=70%, height=70% }

Транслировала файл программы в объектный файл, выполнила компановку объектного файла, 
получила исполняемый файл программы и провреила ее работу.

![Запуск программы lab05-1.asm](image/05.png){ #fig:005 width=70%, height=70% }

Для упрощения написания программ часто встречающиеся одинаковые участки кода
(такие как, например, вывод строки на экран или выход их программы) можно оформить
в виде подпрограмм и сохранить в отдельные файлы, а во всех нужных местах поставить
вызов нужной подпрограммы. Это позволяет сделать основную программу более удобной
для написания и чтения.

Скачала файл in_out.asm и разместила его в рабочем каталоге. 
Для копирования используется клавиша F5.
Для перемещения используется клавиша F6.

Скопировала lab05-1.asm в lab05-2.asm.

![Копирование файла lab05-1.asm](image/06.png){ #fig:006 width=70%, height=70% }

Написала код программы lab05-2.asm с использованием подпрограмм из
внешнего файла in_out.asm.

![Программа в файле lab05-2.asm](image/07.png){ #fig:007 width=70%, height=70% }

![Запуск программы lab05-2.asm](image/08.png){ #fig:008 width=70%, height=70% }

В файле lab5-2.asm заменила подпрограмму sprintLF на sprint. 
Заново собрала исполняеый файл. 
Теперь после вывода строки она не завершается символом перехода на новую строку.

![Программа в файле lab05-2.asm](image/09.png){ #fig:009 width=70%, height=70% }

![Запуск программы lab05-2.asm](image/10.png){ #fig:010 width=70%, height=70% }

Скопировала программу lab05-1.asm и изменила код, так чтобы она работала по следующему алгоритму:

* вывести приглашение типа “Введите строку:”;

* ввести строку с клавиатуры;

* вывести введённую строку на экран.

![Программа в файле lab05-3.asm](image/11.png){ #fig:011 width=70%, height=70% }

![Запуск программы lab05-3.asm](image/12.png){ #fig:012 width=70%, height=70% }

Аналогично скопировала программу lab05-2.asm и изменила код, но теперь использовал подпрограммы из файла in_out.asm.

![Программа в файле lab05-4.asm](image/13.png){ #fig:017 width=70%, height=70% }

![Запуск программы lab05-4.asm](image/14.png){ #fig:018 width=70%, height=70% }

# Выводы

Научились писать базовые ассемблерные программы. Освоили ассемблерные инструкции mov и int.