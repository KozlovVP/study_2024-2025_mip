---
## Front matter
title: "Отчёт по лабораторной работе №6"
subtitle: "Модель хищник–жертва"
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

Реализовать модель хищник-жертва в xcos и OpenModelica.

# Задание

1. Реализовать модель хищник-жертва в xcos.
2. Реализовать модель хищник-жертва в xcos с помощью блока Modelica.
3. Реализовать модель хищник-жертва в OpenModelica.

# Выполнение лабораторной работы

Установил контекст в xcos (рис. [-@fig:001])

![Контекст в xcos](image/1.png){ #fig:001 width=70% }

Построил модель хищник-жертва в xcos (рис. [-@fig:002])

![Модель хищник-жертва в xcos](image/2.png){ #fig:002 width=70% }

Поменял параметры блоков интегрирования (рис. [-@fig:003])

![Параметры блоков интегрирования](image/3.png){ #fig:003 width=70% }

Получил график динамики изменения численности хищников и жертв модели Лотки-Вольтерры (рис. [-@fig:004])

![График динамики изменения численности хищников и жертв](image/4.png){ #fig:004 width=70% }

Получил фазовый портрет модели Лотки-Вольтерры (рис. [-@fig:005])

![Фазовый портрет модели Лотки-Вольтерры](image/5.png){ #fig:005 width=70% }

Построил модель хищник-жертва в xcos с помощью блока Modelica (рис. [-@fig:006])

![Модель хищник-жертва в xcos с помощью блока Modelica](image/6.png){ #fig:006 width=70% }

Изменил параметры блока Modelica (рис. [-@fig:007])

![Параметры блока Modelica](image/7.png){ #fig:007 width=70% }

Записал код для блока Modelica (рис. [-@fig:008])

![Код для блока Modelica](image/8.png){ #fig:008 width=70% }

Получил аналогичный график динамики изменения численности хищников и жертв модели Лотки-Вольтерры (рис. [-@fig:009])

![График динамики изменения численности хищников и жертв](image/9.png){ #fig:009 width=70% }

Записал код в OpenModelica (рис. [-@fig:010])

![Код в OpenModelica](image/10.png){ #fig:010 width=70% }

Получил аналогичный график динамики изменения численности хищников и жертв модели Лотки-Вольтерры (рис. [-@fig:011])

![График динамики изменения численности хищников и жертв](image/11.png){ #fig:011 width=70% }

Получил фазовый портрет модели Лотки-Вольтерры (рис. [-@fig:012])

![Фазовый портрет модели Лотки-Вольтерры](image/12.png){ #fig:012 width=70% }

# Выводы

Реализовал модель хищник-жертва в xcos и OpenModelica.