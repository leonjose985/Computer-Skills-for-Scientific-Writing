---
## Front matter
lang: ru-RU
title: Презентация по лабораторной работе №1
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

Освоение системы вёрстки LaTeX критически важно для исследователей, так как это профессиональный стандарт для подготовки научных статей.

## Объект и предмет исследования

- Дистрибутив TeX Live
- Пакетный менеджер операционной системы
- Операционная система Ubuntu

## Цели и задачи

Освоить базовые принципы работы с системой компьютерной вёрстки LaTeX и установить дистрибутив TeX Live.

## Материалы и методы

- Дистрибутив TeX Live
- Команды `apt`, `pdflatex`
- Операционная система Ubuntu

# Результаты

## Установка TeX Live

Установка выполнена с помощью пакетного менеджера:
```bash
sudo apt install texlive-full
```

## Проверка установки

Корректность установки подтверждена командой:
```bash
pdflatex --version
```

## Создание первого LaTeX-документа
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
Primer documento en LaTeX.
\end{document}
```

## Использование математических формул

Изучены основные способы ввода формул в режиме отображения:
```latex
\[
E = mc^2
\]
```

## Компиляция документа

Для компиляции использовалась команда:
```bash
pdflatex laboratorio1.tex
```

В результате получен файл `laboratorio1.pdf` с корректным форматированием.

# Выводы

## Освоенные технологии и умения

- Установка и настройка дистрибутива TeX Live
- Создание LaTeX-документов
- Работа со структурой документа (`\documentclass`, `\section`, `\maketitle`)
- Ввод математических формул и специальных символов
- Компиляция документов в формат PDF
