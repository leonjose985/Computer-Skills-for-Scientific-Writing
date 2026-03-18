---
## Front matter
title: "Отчёт по лабораторной работе №6"
subtitle: "Computer Skills for Scientific Writing"
author: "Хосе Фернандо Леон Атупанья"

## Generic options
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true
toc-depth: 2
lof: true
lot: true
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt

## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
    - spelling=modern
    - babelshorthands=true
polyglossia-otherlangs:
  name: english

## I18n babel
babel-lang: russian
babel-otherlangs: english

## Fonts
mainfont: Times New Roman
romanfont: Times New Roman
sansfont: Arial
monofont: Courier New

mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=1.0
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=1.0
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase

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
  - \usepackage{float}
  - \floatplacement{figure}{H}
---

# Цель работы

Освоить работу с библиографией в LaTeX, изучить создание и использование BibTeX-файлов, научиться применять различные стили цитирования с помощью пакетов **natbib** и **biblatex**, а также понять различия между двумя подходами к управлению библиографией.

# Ход выполнения

## Тестирование примеров с `natbib` и `biblatex`

Были протестированы оба подхода к управлению библиографией. Для **natbib** применяется последовательность компиляции LaTeX → BibTeX → LaTeX → LaTeX, тогда как для **biblatex** требуется последовательность LaTeX → Biber → LaTeX. Был подготовлен документ с авторско-годовым стилем цитирования на основе пакета **natbib** с опцией `plainnat`.

Исходный код документа с подключением пакета **natbib** и командами цитирования приведён на скриншоте:

![Исходный код документа с пакетом natbib](image/01.png){ #fig:001 width=70% }

Результат компиляции демонстрирует корректное отображение библиографии в стиле `plainnat` с текстовыми и скобочными цитатами:

![Результат PDF: библиография в стиле plainnat](image/02.png){ #fig:002 width=70% }

## Создание новых записей в BibTeX-файле

В файл `learnlatex.bib` были добавлены две новые записи: статья Эйнштейна 1905 года и книга Кнута 1984 года. Для каждой записи были заполнены обязательные поля: `author`, `title`, `year`, а также специфические поля в зависимости от типа источника (`journal`, `volume` для статьи и `publisher` для книги).

Содержимое BibTeX-файла с новыми записями показано на скриншоте:

![Новые записи в BibTeX-файле](image/03.png){ #fig:003 width=70% }

Исходный код документа LaTeX с использованием новых цитат и результат их отображения в PDF приведены на скриншоте:

![Использование новых цитат в документе и результат PDF](image/04.png){ #fig:004 width=70% }

## Цитирование отсутствующей записи в базе данных

Была проверена реакция системы на цитирование источника, отсутствующего в BibTeX-файле. При добавлении команды `\cite{Nonexistent2023}` компиляция завершилась успешно, однако в логе были зафиксированы предупреждения об отсутствующих ссылках, а в тексте документа вместо корректной цитаты отобразился идентификатор в жирном начертании.

Исходный код с цитированием несуществующей записи показан на скриншоте:

![Исходный код с цитированием несуществующей записи](image/05.png){ #fig:005 width=70% }

Предупреждения компилятора в логе компиляции об отсутствующих ссылках приведены на скриншоте:

![Предупреждения в логе компиляции об отсутствующих ссылках](image/06.png){ #fig:006 width=70% }

## Числовой стиль цитирования в `natbib` и `biblatex`

Был протестирован числовой стиль цитирования в обоих подходах. Для **natbib** используется опция `numbers` при загрузке пакета: `\usepackage[numbers]{natbib}`. Для **biblatex** числовой стиль задаётся параметром `style=numeric` при подключении пакета. В обоих случаях цитаты отображаются в виде числовых индексов в квадратных скобках.

Исходный код документа с пакетом **natbib** в числовом режиме приведён на скриншоте:

![Исходный код natbib с опцией numbers](image/07.png){ #fig:007 width=70% }

Результат компиляции демонстрирует числовые цитаты в квадратных скобках:

![Результат PDF: числовые цитаты в стиле natbib](image/08.png){ #fig:008 width=70% }

Аналогичный результат с использованием **biblatex** и параметра `style=numeric` показан на скриншоте:

![Исходный код и результат biblatex с style=numeric](image/09.png){ #fig:009 width=70% }

Итоговое сравнение двух подходов — **natbib** и **biblatex** — с числовым стилем цитирования представлено на скриншоте:

![Сравнение результатов natbib и biblatex](image/10.png){ #fig:010 width=70% }

# Выводы

В ходе выполнения лабораторной работы были успешно освоены ключевые аспекты работы с библиографией в LaTeX:

- изучены два основных подхода к управлению цитированием: традиционный BibTeX с пакетом **natbib** (последовательность LaTeX → BibTeX → LaTeX → LaTeX) и современный **biblatex** с Biber (LaTeX → Biber → LaTeX);
- приобретены практические навыки создания и редактирования BibTeX-файлов с заполнением обязательных и специфических полей для различных типов источников;
- освоено использование авторско-годового и числового стилей цитирования, а также понимание различий в синтаксисе команд между двумя подходами;
- изучено поведение системы при ссылках на отсутствующие источники: компиляция завершается с предупреждениями, а в документе отображается идентификатор вместо корректной цитаты.

Полученные знания позволяют эффективно управлять библиографическими ссылками в научных работах, выбирая оптимальный подход в зависимости от требований издания или журнала.