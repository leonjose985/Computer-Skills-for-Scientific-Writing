---
title: "Отчёт по лабораторной работе №5"
subtitle: "Computer Skills for Scientific Writing"
author: "Хосе Фернандо Леон Атупанья"
lang: ru-RU
toc-title: "Содержание"
bibliography: cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl
toc: true
toc_depth: 2
lof: true
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
polyglossia-lang:
  name: russian
  options:
  - spelling=modern
  - babelshorthands=true
polyglossia-otherlangs:
  name: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
indent: true
header-includes:
  - \linepenalty=10
  - \interlinepenalty=0
  - \hyphenpenalty=50
  - \exhyphenpenalty=50
  - \binoppenalty=700
  - \relpenalty=500
  - \clubpenalty=150
  - \widowpenalty=150
  - \displaywidowpenalty=50
  - \brokenpenalty=100
  - \predisplaypenalty=10000
  - \postdisplaypenalty=0
  - \floatingpenalty = 20000
  - \raggedbottom
  - \usepackage{float}
  - \floatplacement{figure}{H}
---

# Цель работы

Изучить структуру и правильный способ создания таблиц в LaTeX, освоить различные типы выравнивания, объединения ячеек и форматирования таблиц для научных работ.

# Выполнение лабораторной работы

## Базовая таблица с различными типами колонок

В качестве отправной точки была создана базовая таблица с тремя колонками, использующая различные типы выравнивания: левое (`l`), абзацное (`p`) и правое (`r`). Были опробованы вертикальные и горизонтальные линии для оформления границ таблицы
(см. рис. [-@fig:001], [-@fig:002]).

![Базовая таблица с разными типами колонок](img/1.1.PNG){#fig:001}

![Таблица с вертикальными и горизонтальными линиями](img/1.2.PNG){#fig:002}

## Эксперименты с выравниванием колонок

Были опробованы различные комбинации типов выравнивания: левое (`l`), центральное (`c`) и правое (`r`). Эксперимент позволил наглядно сравнить поведение каждого типа при различных категориях данных — текстовых, числовых и смешанных
(см. рис. [-@fig:003], [-@fig:004]).

![Таблица с выравниванием l-c-r](img/2.1.PNG){#fig:003}

![Различные типы данных в разных выравниваниях](img/2.2.PNG){#fig:004}

## Поведение таблицы при недостатке элементов в строке

Было изучено поведение компилятора при наличии строки с меньшим числом элементов, чем объявлено колонок. LaTeX не выдаёт ошибку, а оставляет соответствующие ячейки пустыми, сохраняя структуру таблицы
(см. рис. [-@fig:005], [-@fig:006]).

![Код таблицы с недостающими элементами](img/3.1.PNG){#fig:005}

![Результат компиляции — пустые ячейки](img/3.2.PNG){#fig:006}

## Поведение таблицы при избытке элементов в строке

В отличие от предыдущего случая, при наличии большего числа элементов, чем объявлено колонок, LaTeX прерывает компиляцию с ошибкой `Extra alignment tab has been changed to \cr`. Это поведение было воспроизведено и задокументировано
(см. рис. [-@fig:007], [-@fig:008]).

![Код с избыточными элементами в строке](img/4.1.PNG){#fig:007}

![Сообщение об ошибке компиляции](img/4.2.PNG){#fig:008}

## Объединение ячеек с командой \multicolumn

Была изучена команда `\multicolumn` для горизонтального объединения ячеек таблицы. Команда применялась для создания объединённых заголовков и специальных строк, охватывающих несколько колонок одновременно
(см. рис. [-@fig:009], [-@fig:010]).

![Объединение ячеек для заголовка таблицы](img/5.1.PNG){#fig:009}

![Объединение двух ячеек в одной строке](img/5.2.PNG){#fig:010}

# Выводы

В ходе выполнения лабораторной работы были приобретены необходимые знания и навыки для создания и форматирования таблиц в LaTeX. Были освоены различные типы выравнивания колонок (`l`, `c`, `r`, `p`), изучена команда `\multicolumn` для горизонтального объединения ячеек, а также выяснено поведение системы при структурных ошибках в таблице: при недостатке элементов LaTeX оставляет пустые ячейки, тогда как при избытке — прерывает компиляцию с ошибкой. Полученные навыки являются основой для создания профессионально оформленных таблиц в научных и технических документах.

# Список литературы{.unnumbered}

1. [Tables — Overleaf](https://www.overleaf.com/learn/latex/Tables)
2. [multicolumn command — LaTeX Wiki](https://en.wikibooks.org/wiki/LaTeX/Tables#Spanning)
3. [booktabs package documentation](https://ctan.org/pkg/booktabs)
