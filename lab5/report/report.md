---
## Front matter
title: "Отчёт по лабораторной работе №5"
subtitle: "Конфигурирование VLAN"
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

Получить основные навыки по настройке VLAN на коммутаторах сети.

# Задание

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

# Выполнение лабораторной работы

Поднял trunk-порты на msk-donskaya-vpkozlov-sw-1 (рис. [-@fig:001])

![Создание trunk-портов на msk-donskaya-vpkozlov-sw-1](image/1.png){ #fig:001 width=70% }

Поднял trunk-порты на msk-donskaya-vpkozlov-sw-2 (рис. [-@fig:002])

![Создание trunk-портов на msk-donskaya-vpkozlov-sw-2](image/2.png){ #fig:002 width=70% }

Поднял trunk-порты на msk-donskaya-vpkozlov-sw-3 (рис. [-@fig:003])

![Создание trunk-портов на msk-donskaya-vpkozlov-sw-3](image/3.png){ #fig:003 width=70% }

Поднял trunk-порты на msk-donskaya-vpkozlov-sw-4 (рис. [-@fig:004])

![Создание trunk-портов на msk-donskaya-vpkozlov-sw-4](image/4.png){ #fig:004 width=70% }

Поднял trunk-порты на msk-pavlovskaya-vpkozlov-sw-1 (рис. [-@fig:005])

![Создание trunk-портов на msk-pavlovskaya-vpkozlov-sw-1](image/5.png){ #fig:005 width=70% }

Сконфигурировал VLAN на msk-donskaya-vpkozlov-sw-1 (рис. [-@fig:006])

![Конфигурирование VLAN на msk-donskaya-vpkozlov-sw-1](image/6.png){ #fig:006 width=70% }

Настроил VLAN-порты (рис. [-@fig:007])

![Настройка VLAN-портов](image/7.png){ #fig:007 width=70% }

Настроил VTP сервер на msk-donskaya-vpkozlov-sw-1 (рис. [-@fig:008])

![VTP сервер на msk-donskaya-vpkozlov-sw-1](image/8.png){ #fig:008 width=70% }

Сделал msk-donskaya-vpkozlov-sw-2 клиентом VTP (рис. [-@fig:009])

![Клиент VTP msk-donskaya-vpkozlov-sw-2](image/9.png){ #fig:009 width=70% }

Сделал msk-donskaya-vpkozlov-sw-3 клиентом VTP (рис. [-@fig:010])

![Клиент VTP msk-donskaya-vpkozlov-sw-3](image/10.png){ #fig:010 width=70% }

Сделал msk-donskaya-vpkozlov-sw-4 клиентом VTP (рис. [-@fig:011])

![Клиент VTP msk-donskaya-vpkozlov-sw-4](image/11.png){ #fig:011 width=70% }

Сделал msk-pavlovskaya-vpkozlov-sw-1 клиентом VTP (рис. [-@fig:012])

![Клиент VTP msk-pavlovskaya-vpkozlov-sw-1](image/12.png){ #fig:012 width=70% }

Сконфигурировал диапазоны портов для msk-donskaya-vpkozlov-sw-4 (рис. [-@fig:013])

![Диапазоны портов для msk-donskaya-vpkozlov-sw-4](image/13.png){ #fig:013 width=70% }

Сконфигурировал диапазоны портов для msk-pavlovskaya-vpkozlov-sw-1 (рис. [-@fig:014])

![Диапазоны портов для msk-pavlovskaya-vpkozlov-sw-1](image/14.png){ #fig:014 width=70% }

Сконфигурировал диапазоны портов для msk-donskaya-vpkozlov-sw-2 (рис. [-@fig:015])

![Диапазоны портов для msk-donskaya-vpkozlov-sw-2](image/15.png){ #fig:015 width=70% }

Сконфигурировал диапазоны портов для msk-donskaya-vpkozlov-sw-3 (рис. [-@fig:016])

![Диапазоны портов для msk-donskaya-vpkozlov-sw-3](image/16.png){ #fig:016 width=70% }

Указал ip-адреса для сервера web (рис. [-@fig:017])

![ip-адреса для сервера web](image/17.png){ #fig:017 width=70% }

Указал ip-адреса для сервера file (рис. [-@fig:018])

![ip-адреса для сервера file](image/18.png){ #fig:018 width=70% }

Указал ip-адреса для сервера mail (рис. [-@fig:019])

![ip-адреса для сервера mail](image/19.png){ #fig:019 width=70% }

Указал ip-адреса на dk-donskaya-1 (рис. [-@fig:020])

![ip-адреса на dk-donskaya-1](image/20.png){ #fig:020 width=70% }

Пропинговал другие ПК (рис. [-@fig:021])

![Отправка и получение пакетов от других ПК](image/21.png){ #fig:021 width=70% }

# Выводы

Получил основные навыки по настройке VLAN на коммутаторах сети.

# Контрольные вопросы

1. Какая команда используется для просмотра списка VLAN на сетевом устройстве?

Команда `show vlan`.

2. Охарактеризуйте VLAN Trunking Protocol (VTP). Приведите перечень
команд с пояснениями для настройки и просмотра информации о VLAN.

Протокол VTP (англ. VLAN Trunking Protocol) — протокол ЛВС, служащий для обмена информацией о VLAN (виртуальных сетях), имеющихся на выбранном транковом порту. Разработан и используется компанией Cisco.


* show vlan — выводит подробный список номеров и имён VLAN, активных на коммутаторе, а также портов, назначенных в каждую из них;

* switchport access vlan vlan_number -  команды для назначения отдельных портов в сети VLAN;

* switchport access vlan vlan_number - команды для назначения диапазонов портов в сети VLAN.

3. Охарактеризуйте Internet Control Message Protocol (ICMP). Опишите формат пакета ICMP.

Протокол Internet Control Message Protocol (ICMP) – это набор коммуникационных правил, которые устройства используют для распространения информации об ошибках передачи данных в сети.
При обмене сообщениями между отправителем и получателем могут возникнуть непредвиденные ошибки. Например, сообщения могут быть слишком длинными или пакеты данных могут приходить не по порядку, поэтому получатель не может их организовать.

Формат пакета ICMP включает следующие поля:

* Идентификатор (обычно это идентификатор процесса) и номер по порядку (увеличивается на 1 при посылке каждого пакета). Эти поля служат для того, чтобы отправитель мог связать в пары запросы и отклики.

* Тип определяет, является ли этот пакет запросом (8) или откликом (0).

* Контрольная сумма представляет собой 16-разрядное дополнение по модулю 1 контрольной суммы всего ICMP-сообщения, начиная с поля тип.

* Данные служит для записи информации, возвращаемой отправителю.

4. Охарактеризуйте Address Resolution Protocol (ARP). Опишите формат
пакета ARP.

ARP - протокол разрешения адресов (Address Resolution Protocol) является протоколом третьего (сетевого) уровня модели OSI, используется для преобразования IP-адресов в MAC-адреса, играет важную функцию в множественном доступе сетей.

Формат сообщения ARP включает следующие поля:

* Тип оборудования. Размер поля равен 2 байтам. Определяет тип оборудования, используемое для передачи сообщения. Наиболее распространённый тип оборудования — Ethernet. Значение Ethernet равно 1.

* Тип протокола. Указывает, какой протокол использовался для передачи сообщения. Значение этого поля равно 2048, что указывает на IPv4.

* Длина аппаратного адреса. Показывает длину сетевого адреса в байтах. Размер MAC-адреса Ethernet составляет 6 байт.

* Длина адреса протокола. Показывает размер IP-адреса в байтах. Размер IP-адреса равен 4 байтам.

* Операционный закон. Указывает тип сообщения. Если значение этого поля равно 1, то это сообщение-запрос, а если значение этого поля равно 2, то это ответное сообщение.

* Аппаратный адрес отправителя. Содержит MAC-адрес устройства, передающего сообщение.

5. Что такое MAC-адрес? Какова его структура?

MAC-адрес — это уникальный код, присвоенный производителем сетевому устройству (например, беспроводному сетевому адаптеру или ethernet-адаптеру). MAC — это сокращение от Media Access Control. Предполагается, что каждый код является уникальным для определённого устройства.
MAC-адрес состоит из шести групп по два символа, разделённых двоеточиями, например, 00:1B:44:11:3A:B7.

# Список литературы
1. 802.1D-2004 - IEEE Standard for Local and Metropolitan Area Networks.
Media Access Control (MAC) Bridges : тех. отч. / IEEE. — 2004. — С. 1—
277. — DOI: 10.1109/IEEESTD.2004.94569. — URL: http://ieeexplore.
ieee.org/servlet/opac?punumber=9155.
2. 802.1Q - Virtual LANs. — URL: http://www.ieee802.org/1/pages/802.
1Q.html.
3. A J. Packet Tracer Network Simulator. — Packt Publishing, 2014. —
ISBN 9781782170426. — URL: https://books.google.com/books?id=
eVOcAgAAQBAJ&dq=cisco+packet+tracer&hl=es&source=gbs_navlinks_
s.
4. Cotton M., Vegoda L. Special Use IPv4 Addresses : RFC / RFC Editor. —
01.2010. — С. 1—11. — № 5735. — DOI: 10.17487/rfc5735. — URL: https:
//www.rfc-editor.org/info/rfc5735.
5. Droms R. Dynamic Host Configuration Protocol : RFC / RFC Editor. —
03.1997. — С. 1—45. — № 2136. — DOI: 10.17487/rfc2131. — URL: https:
//www.ietf.org/rfc/rfc2131.txt%20https://www.rfc-editor.org/
info/rfc2131.
6. McPherson D., Dykes B. VLAN Aggregation for Efficient IP Address
Allocation, RFC 3069. — 2001. — URL: http : / / www . ietf . org / rfc /
rfc3069.txt.
7. Moy J. OSPF Version 2 : RFC / RFC Editor. — 1998. — С. 244. — DOI: 10.
17487/rfc2328. — URL: https://www.rfc-editor.org/info/rfc2328.
8. NAT Order of Operation. — URL: https://www.cisco.com/c/en/us/
support/docs/ip/network-address-translation-nat/6209-5.html.
9. NAT: вопросы и ответы / Сайт поддержки продуктов и технологий
компании Cisco. — URL: https://www.cisco.com/cisco/web/support/
RU/9/92/92029_nat-faq.html.
10. Neumann J. C. Cisco Routers for the Small Business A Practical Guide for
IT Professionals. — Apress, 2009.
