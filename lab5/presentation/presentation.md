---
## Front matter
lang: ru-RU
title: Лабораторная Работа №5
subtitle: Конфигурирование VLAN
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

Получить основные навыки по настройке VLAN на коммутаторах сети.

## Задание

1. На коммутаторах сети настроить Trunk-порты на соответствующих интерфейсах, связывающих коммутаторы между
собой.
2. Коммутатор msk-donskaya-sw-1 настроить как VTP-сервер и прописать на
нём номера и названия VLAN согласно таблице.
3. Коммутаторы msk-donskaya-sw-2 — msk-donskaya-sw-4, mskpavlovskaya-sw-1 настроить как VTP-клиенты, на интерфейсах указать
принадлежность к соответствующему VLAN.
4. На серверах прописать IP-адреса, как указано в таблице.
5. На оконечных устройствах указать соответствующий адрес шлюза и прописать статические IP-адреса из диапазона соответствующей сети, следуя регламенту выделения ip-адресов.
6. Проверить доступность устройств, принадлежащих одному VLAN, и недоступность устройств, принадлежащих разным VLAN.
7. При выполнении работы необходимо учитывать соглашение об именовании

## Поднял trunk-порты на msk-donskaya-vpkozlov-sw-1

![Создание trunk-портов на msk-donskaya-vpkozlov-sw-1](image/1.png){ #fig:001 width=70% }

## Поднял trunk-порты на msk-donskaya-vpkozlov-sw-2

![Создание trunk-портов на msk-donskaya-vpkozlov-sw-2](image/2.png){ #fig:002 width=70% }

## Поднял trunk-порты на msk-donskaya-vpkozlov-sw-3

![Создание trunk-портов на msk-donskaya-vpkozlov-sw-3](image/3.png){ #fig:003 width=70% }

## Поднял trunk-порты на msk-donskaya-vpkozlov-sw-4

![Создание trunk-портов на msk-donskaya-vpkozlov-sw-4](image/4.png){ #fig:004 width=70% }

## Поднял trunk-порты на msk-pavlovskaya-vpkozlov-sw-1

![Создание trunk-портов на msk-pavlovskaya-vpkozlov-sw-1](image/5.png){ #fig:005 width=70% }

## Сконфигурировал VLAN на msk-donskaya-vpkozlov-sw-1

![Конфигурирование VLAN на msk-donskaya-vpkozlov-sw-1](image/6.png){ #fig:006 width=70% }

## Настроил VLAN-порты

![Настройка VLAN-портов](image/7.png){ #fig:007 width=70% }

## Настроил VTP сервер на msk-donskaya-vpkozlov-sw-1

![VTP сервер на msk-donskaya-vpkozlov-sw-1](image/8.png){ #fig:008 width=70% }

## Сделал msk-donskaya-vpkozlov-sw-2 клиентом VTP

![Клиент VTP msk-donskaya-vpkozlov-sw-2](image/9.png){ #fig:009 width=70% }

## Сделал msk-donskaya-vpkozlov-sw-3 клиентом VTP

![Клиент VTP msk-donskaya-vpkozlov-sw-3](image/10.png){ #fig:010 width=70% }

## Сделал msk-donskaya-vpkozlov-sw-4 клиентом VTP

![Клиент VTP msk-donskaya-vpkozlov-sw-4](image/11.png){ #fig:011 width=70% }

## Сделал msk-pavlovskaya-vpkozlov-sw-1 клиентом VTP

![Клиент VTP msk-pavlovskaya-vpkozlov-sw-1](image/12.png){ #fig:012 width=70% }

## Сконфигурировал диапазоны портов для msk-donskaya-vpkozlov-sw-4

![Диапазоны портов для msk-donskaya-vpkozlov-sw-4](image/13.png){ #fig:013 width=70% }

## Сконфигурировал диапазоны портов для msk-pavlovskaya-vpkozlov-sw-1

![Диапазоны портов для msk-pavlovskaya-vpkozlov-sw-1](image/14.png){ #fig:014 width=70% }

## Сконфигурировал диапазоны портов для msk-donskaya-vpkozlov-sw-2

![Диапазоны портов для msk-donskaya-vpkozlov-sw-2](image/15.png){ #fig:015 width=70% }

## Сконфигурировал диапазоны портов для msk-donskaya-vpkozlov-sw-3

![Диапазоны портов для msk-donskaya-vpkozlov-sw-3](image/16.png){ #fig:016 width=70% }

## Указал ip-адреса для сервера web

![ip-адреса для сервера web](image/17.png){ #fig:017 width=70% }

## Указал ip-адреса для сервера file

![ip-адреса для сервера file](image/18.png){ #fig:018 width=70% }

## Указал ip-адреса для сервера mail

![ip-адреса для сервера mail](image/19.png){ #fig:019 width=70% }

## Указал ip-адреса на dk-donskaya-1

![ip-адреса на dk-donskaya-1](image/20.png){ #fig:020 width=70% }

## Пропинговал другие ПК

![Отправка и получение пакетов от других ПК](image/21.png){ #fig:021 width=70% }

## Выводы

Получил основные навыки по настройке VLAN на коммутаторах сети.