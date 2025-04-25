---
## Front matter
lang: ru-RU
title: Лабораторная Работа №11
subtitle: Модель системы массового обслуживания M|M|1
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

Реализовать модель M|M|1 в CPN tools.

## Задание

1. Реализовать в CPN tools модель системы массового обслуживания M|M|1.
2. Настроить мониторинг параметров моделируеой системы и нарисовать графики очереди.

## Граф сети системы обработки заявки в очереди

![Граф сети системы обработки заявки в очереди](image/1.png){ #fig:001 width=70% }

## Граф генератора заявок системы

![Граф генератора заявок системы](image/2.png){ #fig:002 width=70% }

## Граф процесса обработки заявок на сервере системы

![Граф процесса обработки заявок на сервере системы](image/3.png){ #fig:003 width=70% }

## Задал декларацию системы

![Декларация системы](image/4.png){ #fig:004 width=70% }

## Параметры элементов основного графика системы обработки заявок в очереди

![Параметры элементов основного графика системы обработки заявок в очереди](image/5.png){ #fig:005 width=70% }

## Параметры элементов генератора заявок системы

![Параметры элементов генератора заявок системы](image/6.png){ #fig:006 width=70% }

## Параметры элементов обработчика заявок системы

![Параметры элементов обработчика заявок системы](image/7.png){ #fig:007 width=70% }

## Написал функцию Predicate монитора Ostanowka

![Функция Predicate монитора Ostanowka](image/8.png){ #fig:008 width=70% }

## Написал функцию Observer монитора Queue Delay

![Функция Observer монитора Queue Delay](image/9.png){ #fig:009 width=70% }

## Получил следующий файл Queue_Delay.log

![Файл Queue_Delay.log](image/10.png){ #fig:010 width=70% }

## Построил график изменения задержки в очереди

![График изменения задержки в очереди](image/11.png){ #fig:011 width=70% }

## Написал функцию Observer монитора Queue Delay Real

![Функция Observer монитора Queue Delay Real](image/12.png){ #fig:012 width=70% }

## Получил следующий файл Queue_Delay_Real.log

![Файл Queue_Delay_Real.log](image/13.png){ #fig:013 width=70% }

## Написал функцию Observer монитора Long Delay Time

![Функция Observer монитора Long Delay Time](image/14.png){ #fig:014 width=70% }

## Получил следующий файл Long_Delay_Time.log

![Файл Long_Delay_Time.log](image/15.png){ #fig:015 width=70% }

## Построил график: периоды времени, когда значения задержки в очереди превышали заданное значение

![Периоды времени, когда значения задержки в очереди превышали заданное значение](image/16.png){ #fig:016 width=70% }

## Выводы

Реализовал модель M|M|1 в CPN tools.