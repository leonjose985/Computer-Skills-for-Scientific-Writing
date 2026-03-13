---
title: "Отчёт по лабораторной работе №4"
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

Изучить структуру и правильный способ размещения изображений в научных работах, чтобы приобрести хорошие навыки и умения в объективном и нейтральном написании формальных исследований.

# Выполнение лабораторной работы

## Включение собственных изображений

В качестве первого задания стандартные демонстрационные изображения были заменены на собственные. Была изучена базовая команда включения графики в документ LaTeX и проверена корректность отображения файлов в различных форматах
(см. рис. [-@fig:001], [-@fig:002]).

![Включение собственного изображения (1)](image/1.1.PNG){#fig:001}

![Включение собственного изображения (2)](image/1.2.PNG){#fig:002}

## Параметры масштабирования изображений

Были изучены параметры команды `\includegraphics`: `height`, `width`, `angle` и `scale`. Каждый из параметров был опробован на практике для понимания их влияния на отображение графики в документе
(см. рис. [-@fig:003], [-@fig:004]).

![Параметры height, width и angle](image/2.1.PNG){#fig:003}

![Параметр scale и его комбинации](image/2.2.PNG){#fig:004}

## Ширина изображения относительно текста и строки

Параметр `width` был использован для задания размера изображений относительно ширины текста (`\textwidth`) и ширины строки (`\linewidth`). Было проверено поведение обоих вариантов при включении и отключении опции двух столбцов в документе
(см. рис. [-@fig:005], [-@fig:006]).

![Изображение с шириной относительно textwidth](image/3.1.PNG){#fig:005}

![Изображение с шириной относительно linewidth](image/3.2.PNG){#fig:006}

## Плавающие объекты и спецификаторы положения

С помощью пакета `lipsum` был создан достаточно длинный текст для демонстрации поведения плавающих объектов. Были опробованы различные спецификаторы положения: `h`, `t`, `b`, `p` и `H`. Было изучено их взаимодействие и влияние на расположение фигур относительно текста
(см. рис. [-@fig:007], [-@fig:008]).

![Спецификаторы положения h, t и b](image/4.1.PNG){#fig:007}

![Спецификаторы положения p и H](image/4.2.PNG){#fig:008}

## Нумерованные разделы и команда \label

В тестовый документ были добавлены новые разделы, подразделы и нумерованные списки. Проводились эксперименты по определению необходимого количества компиляций для корректной работы команд `\label` и `\ref`
(см. рис. [-@fig:009], [-@fig:010]).

![Структура разделов и подразделов](image/5.1.PNG){#fig:009}

![Работа команд label и ref после нескольких компиляций](image/5.2.PNG){#fig:010}

## Размещение метки относительно подписи

Было изучено поведение ссылок при размещении команды `\label` до и после команды `\caption`. Эксперимент позволил установить, что метка должна располагаться строго после подписи для корректной нумерации ссылок
(см. рис. [-@fig:011], [-@fig:012]).

![Метка после подписи — корректный результат](image/6.1.PNG){#fig:011}

![Метка перед подписью — некорректный результат](image/6.2.PNG){#fig:012}

## Метка уравнения после закрывающего окружения

Был проведён эксперимент с размещением команды `\label` после завершающей команды окружения `equation`. Было установлено, что в этом случае метка присваивается следующему нумерованному объекту, а не уравнению, что приводит к некорректным ссылкам
(см. рис. [-@fig:013], [-@fig:014]).

![Метка внутри окружения equation — корректный результат](image/7.1.PNG){#fig:013}

![Метка вне окружения equation — некорректный результат](image/7.2.PNG){#fig:014}

# Выводы

В ходе выполнения лабораторной работы были приобретены необходимые знания для размещения изображений и оформления перекрёстных ссылок в научных документах формата LaTeX. Были изучены параметры масштабирования графики (`width`, `height`, `angle`, `scale`), поведение плавающих объектов при различных спецификаторах положения, а также правила корректного использования команд `\label` и `\ref` относительно команд `\caption`. Все поставленные задачи были успешно выполнены.

# Список литературы{.unnumbered}

1. [Inserting Images — Overleaf](https://www.overleaf.com/learn/latex/Inserting_Images)
2. [Floats, Figures and Captions — Overleaf](https://www.overleaf.com/learn/latex/Floats,_figures_and_captions)
3. [Cross Referencing — Overleaf](https://www.overleaf.com/learn/latex/Cross_referencing_sections,_equations_and_floats)
