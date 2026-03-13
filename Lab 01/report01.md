---
# Front matter
title: "Отчёт по лабораторной работе №1"
subtitle: "Computer Skills for Scientific Writing"
author: "Хосе Фернандо Леон Атупанья | НФИмд-01-24"

# Generic options
lang: ru-RU
toc-title: "Содержание"

# Pdf output format
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt

## I18n
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: spanish
  options:
    - variant=mexican

### Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9

## Misc options
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

### 1. Установка дистрибутива TeX Live

В рамках лабораторной работы была выполнена установка дистрибутива TeX Live, который является наиболее полным и универсальным набором инструментов для работы с LaTeX. 

Установка производилась в операционной системе Ubuntu с использованием пакетного менеджера `apt`. Для этого была выполнена следующая команда в терминале:

```bash
sudo apt install texlive-full
