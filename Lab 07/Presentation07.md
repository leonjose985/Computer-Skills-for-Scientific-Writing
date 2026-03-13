---
## Front matter
lang: ru-RU
title: Презентация по лабораторной работе №7
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

Создание презентаций и научных постеров средствами LaTeX обеспечивает профессиональное оформление материалов для конференций и публикаций с точным контролем над структурой и содержанием.

## Объект и предмет исследования

- Класс `beamer` для презентаций
- Пакеты `a0poster`, `beamerposter`, `tikzposter` для постеров
- Управление появлением контента: `\pause`, `\uncover`

## Цели и задачи

Освоить создание презентаций и научных постеров в LaTeX с использованием класса `beamer` и пакетов для постеров.

## Материалы и методы

- Дистрибутив TeX Live
- Класс `beamer`, тема `Copenhagen`
- Пакеты `a0poster`, `multicol`

# Результаты

## Базовая структура презентации Beamer
```latex
\documentclass{beamer}
\usetheme{Copenhagen}
\author{Хосе Леон}
\title{Введение в простые числа}
\begin{document}
\begin{frame}\titlepage\end{frame}
\begin{frame}{Введение}
    Простые числа — строительные блоки арифметики.
\end{frame}
\end{document}
```

## Работа с блоками и списками
```latex
\begin{frame}{Математические понятия}
    \begin{block}{Определение}
        Простое число — натуральное число больше 1...
    \end{block}
    \begin{enumerate}
        \item Первый пункт
        \item Второй пункт
    \end{enumerate}
\end{frame}
```

## Управление появлением контента
```latex
\begin{frame}{Теория множеств}
    Множество — это коллекция объектов.
    \uncover<2->{Пример: $A = \{1, 2, 3\}$.}
    \uncover<3->{Элементы $A$: 1, 2, 3.}
\end{frame}
```

## Создание постера с a0poster
```latex
\documentclass[a0,portrait]{a0poster}
\usepackage{multicol}
\columnsep=100pt
\begin{document}
\begin{multicols}{2}
    \section*{Введение}
    Текст в двух колонках...
\end{multicols}
\end{document}
```

# Выводы

## Освоенные технологии и умения

- Создание динамических презентаций с пошаговым отображением контента
- Использование блоков, списков и колонок в `beamer`
- Разработка профессиональных научных постеров с `a0poster`
- Сравнение трёх методов создания постеров: `a0poster`, `beamerposter`, `tikzposter`
- Подготовка структурированных материалов для конференций и публикаций
