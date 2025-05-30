---
## Front matter
title: "Отчёт по лабораторной работе №15"
subtitle: "Модели обслуживания с приоритетами"
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

Реализовать модели обслуживания с приоритетами и провести анализ результатов.

# Задание

Реализовать с помощью gpss:

- Модель обслуживания механиков на складе
- Модель обслуживания в порту судов двух типов

# Выполнение лабораторной работы

## Модель обслуживания механиков на складе

На фабрике на складе работает один кладовщик, который выдает запасные части механикам, обслуживающим станки. Время, необходимое для удовлетворения запроса, зависит от типа запасной части.Запросы бывают двух категорий. Для первой
категории интервалы времени прихода механиков $420 \pm 360$ сек., время обслуживания -- $300 \pm 90$ сек. Для второй категории интервалы времени прихода механиков $360 \pm 240$ сек., время обслуживания -- $100 \pm 30$ сек
Порядок обслуживания механиков кладовщиком такой: запросы первой категории обслуживаются только в том случае, когда в очереди нет ни одного запроса второй категории. Внутри одной категории дисциплина обслуживания -- "первым пришел -- первым обслужился". Необходимо создать модель работы кладовой, моделирование выполнять в течение восьмичасового рабочего дня.

Есть два различных типа заявок, поступающих на обслуживание к одному устройству. Различаются распределения интервалов приходов и времени обслуживания
для этих типов заявок. Приоритеты запросов задаются путем использования для
операнда `E` блока `GENERATE` запросов второй категории большего значения, чем для
запросов первой категории.

Напишем соответсвующий код для построения модели в gpss (рис. [-@fig:001]).

![Модель обслуживания механиков с приоритетами](image/1.png){#fig:001 width=70%}

Получим следующий отчет (рис. [-@fig:002]).

![Отчет по модели обслуживания механиков с приоритетами](image/2.png){#fig:002 width=70%}

В рамках имитационного моделирования система была проанализирована на протяжении 28800 моделируемых секунд, начиная с момента времени 0. В процессе моделирования использовалось 16 блоков, один одноканальный ресурс (оформляющий оператор) и не применялось ни одно многоканальное устройство. В модели были задействованы следующие элементы: две очереди для разных типов заявок (QS1 и QS2), а также исполнитель — STOCKMAN.

В течение симуляции было зафиксировано 71 обращение первого типа и 83 — второго. Из них до завершения обработки дошли 64 и 81 соответственно. Всего оператором было принято 146 заявок. Эффективность его загрузки составила 96,7%, а средняя продолжительность работы с заявкой — около 190,73 минут.

Очередь QS1, предназначенная для заявок первого типа, показала следующие результаты: максимальное количество клиентов в ожидании достигало 8, а в момент окончания моделирования в очереди находилось 6 заявок. Всего через неё прошло 71 обращение, из которых 4 обрабатывались сразу, без ожидания. В среднем в очереди одновременно находилось около 2,18 заявок, а среднее время нахождения в очереди составило 883 минуты (935 минут, если учитывать только случаи с реальным ожиданием).

Очередь QS2, связанная со вторым типом заявок, демонстрировала менее загруженный характер: максимум 3 заявки в ожидании, и 2 — на момент окончания симуляции. Из 83 заявок только 2 обрабатывались мгновенно. Среднее число клиентов в очереди — менее 0,44, а среднее время ожидания — около 152 минут (почти идентично с учетом и без учета нулевого ожидания).

В заключительной части отчёта приводится информация о следующем ожидаемом событии в модели. Транзакт с номером 141, принадлежащий первому типу заявок, должен активироваться в момент времени 28815,063. Он находится на этапе перехода от пятого блока к шестому, и имеет приоритет, соответствующий первому типу заявок.

## Модель обслуживания в порту судов двух типов

Морские суда двух типов прибывают в порт, где происходит их разгрузка. В порту есть два буксира, обеспечивающих ввод и вывод кораблей из порта. К первому типу судов относятся корабли малого тоннажа, которые требуют использования одного буксира. Корабли второго типа имеют большие размеры, и для их ввода и вывода из порта требуется два буксира. Из-за различия размеров двух типов кораблей необходимы и причалы различного размера. Кроме того, корабли имеют различное время погрузки/разгрузки. 

Требуется построить модель системы, в которой можно оценить время ожидания кораблями каждого типа входа в порт. Время ожидания входа в порт включает время ожидания освобождения причала и буксира. Корабль, ожидающий освобождения причала, не обслуживается буксиром до тех пор, пока не будет предоставлен нужный причал. Корабль второго типа не займёт буксир до тех пор, пока ему не будут доступны оба буксира.

Построим модель обслуживания в порту судов двух типов в gpss (рис. [-@fig:003]).

![Модель обслуживания в порту судов двух типов](image/3.png){#fig:003 width=70%}

Отчет по модели обслуживания в порту судов двух типов в gpss, ч1 (рис. [-@fig:004]).

![Отчет по модели обслуживания в порту судов двух типов в gpss, ч1](image/4.png){#fig:004 width=70%}

Отчет по модели обслуживания в порту судов двух типов в gpss, ч1 (рис. [-@fig:005]).

![Отчет по модели обслуживания в порту судов двух типов в gpss, ч1](image/5.png){#fig:005 width=70%}

Моделирование началось с нулевой отметки по времени и продолжалось до достижения предельного значения в 175200 условных единиц. За это время в работе модели были задействованы 28 логических блоков. Одноканальные ресурсы в данной системе не использовались, в то время как многоканальных устройств было три. Ключевые элементы модели — это два типа судов (TYPE1 и TYPE2) и два соответствующих типа причалов (PRCH1 и PRCH2).

В процессе симуляции система сформировала 1345 запросов для судов первого типа и 446 для второго. Обработке были подвергнуты практически все из них: 1339 первого типа и 365 второго.

Для судов первого типа в очереди одновременно максимально ожидали до четырёх единиц. К окончанию симуляции эта очередь оказалась полностью свободной. Через неё прошло 1345 обращений, из которых 288 были обслужены сразу, минуя ожидание. Средняя загрузка составляла менее одного судна в любой момент времени (0,750), а средняя длительность пребывания в очереди — около 97,7 минут. Если исключить обращения без ожидания, этот показатель возрастает до 124,35 минут.

Аналогичная структура очереди использовалась и для второго типа судов. Здесь также максимум составлял 4 судна, но к завершению работы в очереди оставались ещё два. Через систему прошло 446 таких запросов, 35 из них были приняты моментально. В среднем в очереди находилось около 0,9 судна, а средняя продолжительность ожидания составила 352,6 минут, увеличиваясь до 382,6 минут при исключении мгновенных обработок.

Все обращения от судов первого типа были направлены на группу из шести причалов. Эти причалы показали высокую эффективность работы — почти 97,7% времени они были заняты, при этом средняя продолжительность обработки одного судна составила 5,86 минут.

Для судов второго типа использовалась группа из трёх причалов. Через них прошло 444 обращения, а коэффициент занятости оказался ещё выше — 98,3%. Среднее время взаимодействия с одним судном было значительно меньше — около 2,95 минут.

Система также включала два буксира, которые обеспечивали перемещение судов. Всего за моделируемый период они выполнили 4454 операций, что обусловлено тем, что каждое судно использовало буксирные услуги дважды: один буксир — для судов первого типа и оба буксира — для второго. В среднем уровень их загрузки составил 78,6%, при этом каждая операция занимала около 0,393 минут.

# Выводы

В результате выполнения лабораторной работы удалось реализовать модели обслуживания с приоритетами и провести анализ результатов.