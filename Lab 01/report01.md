---
title: "Отчёт по лабораторной работе №1"
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

Целью данной лабораторной работы является освоение базовых принципов работы с системой вёрстки LaTeX. В ходе выполнения работы необходимо изучить процесс установки дистрибутива TeX Live, познакомиться с основными командами LaTeX, структурой документа и правилами компиляции файлов формата `.tex` в PDF-документ.

Дополнительной задачей является формирование навыков оформления отчётов и научных документов с использованием LaTeX, а также приобретение практического опыта работы с текстовыми редакторами и командной строкой.

# Выполнение лабораторной работы

## Установка дистрибутива TeX Live

В рамках лабораторной работы была выполнена установка дистрибутива TeX Live, который является наиболее полным и универсальным набором инструментов для работы с LaTeX и поддерживается сообществом разработчиков.

Установка производилась с использованием пакетного менеджера операционной системы. Для системы Ubuntu был использован следующий командный интерфейс:
```bash
sudo apt install texlive-full
```

После завершения установки была выполнена проверка корректности работы компилятора LaTeX с помощью команды:
```bash
pdflatex --version
```

Результат выполнения команды подтвердил успешную установку TeX Live и готовность системы к работе с LaTeX-документами
(см. рис. [-@fig:001]).

![Результат команды pdflatex --version](image/1.png){#fig:001}

## Создание первого LaTeX-документа

Был создан файл формата `.tex`, содержащий базовую структуру документа LaTeX. В документе были использованы основные элементы: объявление класса документа (`article`), подключение пакетов для поддержки языка и математических формул, задание заголовка, автора и даты, а также формирование основного содержимого документа.

Пример структуры документа:
```latex
\documentclass{article}
\usepackage[spanish]{babel}
\usepackage{amsmath}

\title{Laboratorio 1}
\author{Jose Fernando Leon Atupanya}
\date{\today}

\begin{document}
\maketitle
\section{Introducción}
Texto del documento.
\end{document}
```

После компиляции файла был получен PDF-документ с корректно отображаемым текстом и структурой
(см. рис. [-@fig:002]).

![Скомпилированный PDF-документ](image/2.png){#fig:002}

## Использование математических формул

В ходе лабораторной работы были изучены основные способы ввода математических выражений в LaTeX: встроенные формулы в тексте, отдельные формулы в режиме отображения, а также нумерованные уравнения.

# Выводы

В ходе выполнения лабораторной работы были освоены основные принципы работы с системой LaTeX и дистрибутивом TeX Live. Были получены следующие навыки и знания: установка и настройка среды LaTeX (TeX Live), создание и компиляция LaTeX-документов, работа с базовой структурой документа (`\documentclass`, `\begin{document}`, `\section`), использование математических формул и специальных символов, а также оформление отчётов в профессиональном и стандартизированном виде.

LaTeX является мощным инструментом для подготовки научных и технических документов, обеспечивающим высокое качество типографики и удобство работы с математическими формулами и структурированным текстом. Несмотря на необходимость изучения синтаксиса команд, LaTeX предоставляет широкие возможности для автоматизации оформления документов, что особенно важно в научной и инженерной деятельности.

# Список литературы{.unnumbered}

1. [TeX Live](https://www.tug.org/texlive/)
2. [LaTeX Project](https://www.latex-project.org/get/)
3. [Ubuntu packages — texlive-full](https://packages.ubuntu.com/texlive-full)
