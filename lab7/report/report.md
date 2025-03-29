---
## Front matter
title: "Отчёт по лабораторной работе №7"
subtitle: "Модель Модель M|M|1|inf"
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

Рассмотреть пример моделирования в *xcos* системы массового обслуживания типа M|M|1|inf.

# Задание

1. Реализовать модель системы массового обслуживания типа M|M|1|inf;
2. Построить график поступления и обработки заявок;
3. Построить график динамики размера очереди.

# Выполнение лабораторной работы

Установил контекст (рис. [-@fig:001])

![Установка контекста](image/1.png){ #fig:001 width=70% }

Создал суперблок, моделирующий поступление заявок (рис. [-@fig:002])

![Суперблок, моделирующий поступление заявок](image/2.png){ #fig:002 width=70% }

Создал суперблок, моделирующий обработку заявок (рис. [-@fig:003])

![Суперблок, моделирующий обработку заявок](image/3.png){ #fig:003 width=70% }

Построил общую модель M|M|1|inf в xcos (рис. [-@fig:004])

![Модель M|M|1|inf в xcos](image/4.png){ #fig:004 width=70% }

Получил график динамики размера очереди (рис. [-@fig:005])

![График динамики размера очереди](image/5.png){ #fig:005 width=70% }

Получил диаграмму поступления и обработки заявок (рис. [-@fig:006])

![Диаграмма поступления и обработки заявок](image/6.png){ #fig:006 width=70% }

# Выводы

Рассмотрел пример моделирования в *xcos* системы массового обслуживания типа M|M|1|inf.