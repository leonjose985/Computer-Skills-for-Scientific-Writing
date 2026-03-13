---
## Front matter
lang: ru-RU
title: Презентация по лабораторной работе №6
subtitle: Дисциплина "Computer Skills for Scientific Writing"
author: Леон А Х Ф
institute: 
  - Кафедра теории вероятностей и кибербезопасности, Российский университет дружбы народов имени Патриса Лумумбы, Москва, Россия
date: 26 октября, 2024, Москва, Россия

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

---

# Информация

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Леон Атупанья Хосе Фернандо
  * студент кафедры теории вероятностей и кибербезопасности
  * Российский университет дружбы народов имени Патриса Лумумбы
  * НФИмд-01-24, 1032249918
  * <https://github.com/>

:::
::: {.column width="30%"}

![](./image/photo.jpg)

:::
::::::::::::::

# Вводная часть

## Актуальность

Грамотная работа с библиографией в LaTeX является обязательным навыком для оформления научных публикаций, обеспечивая корректное цитирование источников и соответствие требованиям журналов.

## Объект и предмет исследования

- Пакеты `natbib` и `biblatex`
- Структура BibTeX-файлов
- Стили цитирования: авторский и числовой

## Цели и задачи

Освоить работу с библиографией в LaTeX, изучить создание и использование BibTeX-файлов, научиться применять различные стили цитирования с помощью пакетов `natbib` и `biblatex`.

## Материалы и методы

- Дистрибутив TeX Live
- Пакеты `natbib` и `biblatex`
- Процессор `bibtex` / `biber`

# Результаты

## Работа с natbib
```latex
\usepackage{natbib}
...
\citet{Graham1995}  % текстовая цитата
\citep{Thomas2008}  % скобочная цитата
\bibliographystyle{plainnat}
\bibliography{learnlatex}
```

## Результат компиляции с natbib

![Список литературы, сформированный natbib](img/1.2.PNG){#fig:001 width=90%}

## Создание новых библиографических записей
```latex
@article{Einstein1905,
  author  = {Albert Einstein},
  title   = {On the Electrodynamics of Moving Bodies},
  journal = {Annalen der Physik},
  year    = {1905},
  volume  = {322},
  number  = {10},
  pages   = {891--921},
  doi     = {10.1002/andp.19053221004},
}
```

## Результат добавления новой записи

![Новая запись в списке литературы](img/2.2.PNG){#fig:002 width=90%}

## Обработка отсутствующих ссылок
```latex
\cite{Nonexistent2023}
```

При компиляции генерируются предупреждения об отсутствующей записи в базе данных.

## Результат при отсутствующей ссылке

![Предупреждения компилятора при отсутствующей ссылке](img/3.2.PNG){#fig:003 width=90%}

## Числовой стиль цитирования: natbib и biblatex

:::::::::::::: {.columns align=center}
::: {.column width="50%"}
```latex
\usepackage[numbers]{natbib}
...
\citep{Graham1995}
% Результат: [1]
```

:::
::: {.column width="50%"}
```latex
\usepackage[style=numeric]{biblatex}
...
\autocite{Thomas2008}
% Результат: [2]
```

:::
::::::::::::::

# Выводы

## Освоенные технологии и умения

- Работа с двумя подходами к библиографии: `natbib` и `biblatex`
- Создание и редактирование BibTeX-файлов
- Применение текстового и скобочного стилей цитирования
- Настройка числового формата цитирования
- Анализ поведения системы при отсутствующих ссылках
