---
## Front matter
title: "Отчёт по лабораторной работе №11"
subtitle: "Модель системы массового обслуживания M|M|1"
author: "Козлов Всеволод Павлович НФИбд-02-22"

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
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: Arial
romanfont: Arial
sansfont: Arial
monofont: Arial
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

Реализовать модель M|M|1 в CPN tools.

# Задание

1. Реализовать в CPN tools модель системы массового обслуживания M|M|1.
2. Настроить мониторинг параметров моделируеой системы и нарисовать графики очереди.

# Выполнение лабораторной работы

Граф сети системы обработки заявки в очереди (рис. [-@fig:001])

![Граф сети системы обработки заявки в очереди](image/1.png){ #fig:001 width=70% }

Граф генератора заявок системы (рис. [-@fig:002])

![Граф генератора заявок системы](image/2.png){ #fig:002 width=70% }

Граф процесса обработки заявок на сервере системы (рис. [-@fig:003])

![Граф процесса обработки заявок на сервере системы](image/3.png){ #fig:003 width=70% }

Задал декларацию системы(рис. [-@fig:004])

![Декларация системы](image/4.png){ #fig:004 width=70% }

Параметры элементов основного графика системы обработки заявок в очереди (рис. [-@fig:005])

![Параметры элементов основного графика системы обработки заявок в очереди](image/5.png){ #fig:005 width=70% }

Параметры элементов генератора заявок системы (рис. [-@fig:006])

![Параметры элементов генератора заявок системы](image/6.png){ #fig:006 width=70% }

Параметры элементов обработчика заявок системы (рис. [-@fig:007])

![Параметры элементов обработчика заявок системы](image/7.png){ #fig:007 width=70% }

Написал функцию Predicate монитора Ostanowka (рис. [-@fig:008])

![Функция Predicate монитора Ostanowka](image/8.png){ #fig:008 width=70% }

Написал функцию Observer монитора Queue Delay (рис. [-@fig:009])

![Функция Observer монитора Queue Delay](image/9.png){ #fig:009 width=70% }

Получил следующий файл Queue_Delay.log (рис. [-@fig:010])

![Файл Queue_Delay.log](image/10.png){ #fig:010 width=70% }

```
#!/usr/bin/gnuplot -persist
# задаём текстовую кодировку,
# тип терминала, тип и размер шрифта

set encoding utf8
set term pngcairo font "Helvetica,9"

# задаём выходной файл графика
set out 'window_1.png'
plot "Queue_Delay.log" using ($4):($1) with lines
```

Построил график изменения задержки в очереди (рис. [-@fig:011])

![График изменения задержки в очереди](image/11.png){ #fig:011 width=70% }

Написал функцию Observer монитора Queue Delay Real (рис. [-@fig:012])

![ФункциЯ Observer монитора Queue Delay Real](image/12.png){ #fig:012 width=70% }

Получил следующий файл Queue_Delay_Real.log (рис. [-@fig:013])

![Файл Queue_Delay_Real.log](image/13.png){ #fig:013 width=70% }

Написал функцию Observer монитора Long Delay Time (рис. [-@fig:014])

![Функция Observer монитора Long Delay Time](image/14.png){ #fig:014 width=70% }

Получил следующий файл Long_Delay_Time.log (рис. [-@fig:015])

![Файл Long_Delay_Time.log](image/15.png){ #fig:015 width=70% }

```
#!/usr/bin/gnuplot -persist
# задаём текстовую кодировку,
# тип терминала, тип и размер шрифта

set encoding utf8
set term pngcairo font "Helvetica,9"

# задаём выходной файл графика
set out 'window_1.png'
set style line 2
plot [0:] [0:1.2] "Long_Delay_Time.log" using ($4):($1) with lines
```

Построил график: периоды времени, когда значения задержки в очереди превышали заданное значение (рис. [-@fig:016])

![Периоды времени, когда значения задержки в очереди превышали заданное значение](image/16.png){ #fig:016 width=70% }

# Выводы

Реализовал модель M|M|1 в CPN tools.