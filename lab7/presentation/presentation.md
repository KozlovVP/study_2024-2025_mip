---
## Front matter
lang: ru-RU
title: Лабораторная Работа №7
subtitle: Модель Модель M|M|1|inf
author:
  - Козлов В.П.
institute:
  - Российский университет дружбы народов им. Патриса Лумумбы, Москва, Россия

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\makeatother'

## Fonts
mainfont: Arial
romanfont: Arial
sansfont: Arial
monofont: Arial
---


## Докладчик


  * Козлов Всеволод Павлович
  * НФИбд-02-22
  * Российский университет дружбы народов
  * [1132226428@pfur.ru]
  
# Выполнение лабораторной работы

## Цель работы

Рассмотреть пример моделирования в *xcos* системы массового обслуживания типа M|M|1|inf.

## Задание

1. Реализовать модель системы массового обслуживания типа M|M|1|inf;
2. Построить график поступления и обработки заявок;
3. Построить график динамики размера очереди.

## Установил контекст

![Установка контекста](image/1.png){ #fig:001 width=70% }

## Создал суперблок, моделирующий поступление заявок

![Суперблок, моделирующий поступление заявок](image/2.png){ #fig:002 width=70% }

## Создал суперблок, моделирующий обработку заявок

![Суперблок, моделирующий обработку заявок](image/3.png){ #fig:003 width=70% }

## Построил общую модель M|M|1|inf в xcos

![Модель M|M|1|inf в xcos](image/4.png){ #fig:004 width=70% }

## Получил график динамики размера очереди

![График динамики размера очереди](image/5.png){ #fig:005 width=70% }

## Получил диаграмму поступления и обработки заявок

![Диаграмма поступления и обработки заявок](image/6.png){ #fig:006 width=70% }

## Выводы

Рассмотрел пример моделирования в *xcos* системы массового обслуживания типа M|M|1|inf.