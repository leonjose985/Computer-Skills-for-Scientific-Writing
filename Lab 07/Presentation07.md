---
marp: true
css: custom-theme.css
title: "Лабораторная работа №7"
subtitle: "Дисциплина: Computer Skills for Scientific Wrinting"
author: Хосе Фернандо Леон Атупанья, НФИмд-01-24, 1032249918
institute: Российский Университет Дружбы Народов, Москва, Россия
date: 26 октобря 2024

---

# **Лабораторная работа № 7**

**Дисциплина**: Computer Skills for Scientific Wrinting

**Тема:** Latex Presentation

**Студент:** Леон Фернандо Хосе Фернандо 

--- 

## **Цель работы**

Освоить создание презентаций и научных постеров в LaTeX с использованием:
- Класса **Beamer** для презентаций
- Пакетов **a0poster**, **beamerposter**, **tikzposter** для постеров

**Задачи:**
1. Изучить структуру презентаций Beamer
2. Освоить управление появлением контента (pause/uncover)
3. Научиться создавать многостолбцовые макеты постеров
4. Сравнить три метода создания постеров

---

# **2. Выполнение лабораторной работы**

Использование темы `Copenhagen` с заголовочным слайдом и тремя содержательными слайдами.

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

---

2. Работа с блоками и списками
Использование окружений block, enumerate и itemize для организации информации.

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
---

## 2. Создание новых библиографических записей
Расширение базы данных learnlatex.bib новыми записями и их использование в документе.
```latex
@article{Einstein1905,
author = {Albert Einstein},
title = {On the Electrodynamics of Moving Bodies},
journal = {Annalen der Physik},
year = {1905},
volume = {322},
number = {10},
pages = {891--921},
doi = {10.1002/andp.19053221004},
}
```

---

## 3. Управление появлением контента
Использование \pause и \uncover

```latex
\begin{frame}{Теория множеств}
    Множество — это коллекция объектов.
    \uncover<2->{Пример: $A = \{1, 2, 3\}$.}
    \uncover<3->{Элементы $A$: 1, 2, 3.}
\end{frame}
```

---
## 4 Создание постера с a0poster
Эксперименты с числовым форматом цитирования в обоих подходах.

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
---

## 5 Создание постера с a0poster
Простой подход для текстовых постеров:
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
---

# **Вывод**
Лабораторная работа успешно выполнена. Были получены практические навыки создания:

Динамических презентаций с пошаговым отображением

Профессиональных научных постеров в трёх различных стилях

Структурированных документов с использованием блоков и колонок

Полученные знания essential для подготовки качественных научных материалов к конференциям и публикациям.


