---
title: "Отчёт по лабораторной работе №2"
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

Освоить базовую структуру документа LaTeX, научиться компилировать `.tex`-файлы в PDF, изучить основные специальные символы LaTeX и их использование. Научиться создавать простые документы, разделять текст на параграфы, применять жёсткие пробелы и правильно использовать комментарии в коде.

# Выполнение лабораторной работы

## Создание первого документа LaTeX

В качестве первого задания был создан файл `first.tex` с минимальной структурой документа LaTeX. Цель — изучить базовое устройство `.tex`-файла и скомпилировать его в PDF с помощью команды `pdflatex` в терминале (см. рис. [-@fig:001]).
```latex
\documentclass{article}
\usepackage[T1]{fontenc}

\begin{document}
Hey world!

This is a first document.
\end{document}
```

![Компиляция первого документа и результат в PDF](image/1.png){#fig:001}

## Добавление комментариев и структурирование документа

На следующем этапе документ был расширен: добавлены параметры класса документа, сноска с помощью команды `\footnote{}`, а также разделение текста на параграфы через пустую строку (см. рис. [-@fig:002]).
```latex
\documentclass[a4paper,12pt]{article}
\usepackage[T1]{fontenc}

\begin{document}
This is a simple document\footnote{with a footnote}.

This is a new paragraph.
\end{document}
```

![Документ со сноской и параграфами](image/2.png){#fig:002}

## Работа со специальными символами и жёсткими пробелами

Был создан отдельный документ для изучения экранирования специальных символов LaTeX (`$`, `%`, `&`, `#`, `_`, `{`, `}`) и применения жёстких пробелов (`~`) для контроля переноса строк (см. рис. [-@fig:003]).
```latex
\documentclass{article}
\usepackage[T1]{fontenc}

\begin{document}
Примеры специальных символов:

- Доллар: \$100
- Процент: 20\%
- Амперсанд: AT\&T
- Решётка: \#tag
- Нижнее подчёркивание: variable\_name
- Фигурные скобки: \{текст\}

Пример жёсткого пробела:
Dr.~House, стр.~45, рис.~1.2.
\end{document}
```

![Результат компиляции документа со специальными символами](image/3.png){#fig:003}

# Выводы

В ходе выполнения лабораторной работы были освоены основные принципы работы с документами LaTeX. Было изучено устройство файла `.tex`: разделение на преамбулу и тело документа, использование команд `\documentclass`, `\usepackage`, `\begin{document}` и `\end{document}`. Получены навыки компиляции через команду `pdflatex` и понимание цепочки преобразования `.tex` → `.pdf`.

Отдельное внимание было уделено правильному экранированию специальных символов (`$`, `%`, `&`, `#`, `_`, `{`, `}`), использованию жёстких пробелов (`~`) для управления переносами, созданию параграфов через пустые строки и добавлению сносок командой `\footnote{}`.

LaTeX предоставляет мощный и точный инструмент для создания структурированных документов. Его синтаксис, хотя и требует внимательности к деталям, позволяет достичь профессионального форматирования, что особенно важно в научных и технических работах. Освоение базовых принципов LaTeX является фундаментом для дальнейшего изучения более сложных возможностей системы.

# Список литературы{.unnumbered}

1. [LaTeX Project](https://www.latex-project.org/get/)
2. [Overleaf — Special Characters](https://www.overleaf.com/learn/latex/Special_characters)
3. [TeX Live](https://www.tug.org/texlive/)
