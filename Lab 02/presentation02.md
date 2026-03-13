---
## Front matter
lang: ru-RU
title: Презентация по лабораторной работе №2
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

Освоение принципов создания документов в LaTeX необходимо для работы с научными публикациями, где точный контроль над форматированием имеет принципиальное значение.

## Объект и предмет исследования

- Структура LaTeX-документа
- Специальные символы и команды
- Жёсткие пробелы и управление параграфами

## Цели и задачи

Освоить принципы создания и компиляции документов в LaTeX, изучить базовую структуру файла, а также научиться работать со специальными символами и управлять оформлением текста.

## Материалы и методы

- Дистрибутив TeX Live
- Команда `pdflatex`
- Операционная система Ubuntu

# Результаты

## Создание первого документа LaTeX
```latex
\documentclass{article}
\usepackage[T1]{fontenc}

\begin{document}
Hey world!

This is a first document.
\end{document}
```

## Структурирование документа с комментариями
```latex
\documentclass[a4paper,12pt]{article}
\usepackage[T1]{fontenc}

\begin{document}
This is a simple document\footnote{with a footnote}.

This is a new paragraph.
\end{document}
```

## Работа со специальными символами
```latex
\documentclass{article}
\usepackage[T1]{fontenc}

\begin{document}
Специальные символы:
- Доллар: \$100
- Процент: 20\%
- Амперсанд: AT\&T
- Решётка: \#tag

Жёсткие пробелы:
Dr.~House, стр.~45, рис.~1.2
\end{document}
```

## Практическое упражнение 2.1.4
```latex
\documentclass[a4paper,12pt]{article}
\usepackage[T1]{fontenc}

\begin{document}
\section*{Exercise 2.1.4}

First paragraph with regular text.

Second paragraph: Dr.~Smith, Prof.~Johnson.
Price: \$50, discount: 15\%, reference: section\#3.
\end{document}
```

# Выводы

## Освоенные технологии и умения

- Создание и компиляция LaTeX-документов в PDF
- Работа со структурой документа: преамбула, тело, окружения
- Использование специальных символов и команд
- Применение жёстких пробелов и управление параграфами
- Чтение и отладка логов LaTeX
