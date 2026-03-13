---
## Front matter
lang: ru-RU
title: Презентация по лабораторной работе №8
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

Создание векторной графики средствами LaTeX позволяет интегрировать точные диаграммы и математические графики непосредственно в научные публикации без потери качества при масштабировании.

## Объект и предмет исследования

- Пакет `TikZ` для программирования графики
- Циклы `\foreach` для повторяющихся элементов
- Рекурсивные алгоритмы для фрактальных структур

## Цели и задачи

Освоить создание векторной графики и диаграмм в LaTeX с использованием пакета `TikZ`, циклов и рекурсивных функций.

## Материалы и методы

- Дистрибутив TeX Live
- Пакет `TikZ` и библиотека `tikzmath`
- Команды `\foreach`, `\draw`, `\fill`

# Результаты

## Создание графа с использованием TikZ
```latex
\begin{tikzpicture}[scale=1.5]
\foreach \angle/\label in {90/A, 30/B, -30/C, -90/D, -150/E, 150/F}
    \node[circle, draw] (\label) at (\angle:2) {\label};
\draw[->] (A) -- (B) node[midway, above] {1};
\draw[->] (B) -- (C) node[midway, above right] {2};
% ... остальные рёбра
\end{tikzpicture}
```

## Результат: граф из шести узлов

![Граф из шести узлов, расположенных по кругу](img/1.1.PNG){#fig:001 width=90%}

## Построение графиков функций
```latex
\begin{tikzpicture}[scale=1.2]
\draw[gray, ->] (-1,0) -- (3,0) node[right] {$x$};
\draw[gray, ->] (0,-1) -- (0,4) node[above] {$y$};
\draw[blue, thick, domain=-1:1.2, samples=50]
    plot (\x, {exp(\x)}) node[right] {$y = e^x$};
\draw[red, thick] (-1,1) -- (3,1) node[right] {$y = 1$};
\draw[green, thick] (1,-1) -- (1,4) node[above] {$x = 1$};
\end{tikzpicture}
```

## Результат: график функции $e^x$

![Координатные оси и графики нескольких функций](img/2.1.PNG){#fig:002 width=90%}

## Генерация ковра Серпинского
```latex
\tikzmath{
    function sierpinskiCarpet(\x, \y, \s, \d) {
        if (\d == 0) then {
            { \fill (\x,\y) rectangle (\x+\s, \y+\s); };
        } else {
            \ns = \s / 3;
            for \i in {0,1,2} {
                for \j in {0,1,2} {
                    if not ((\i==1) && (\j==1)) then {
                        sierpinskiCarpet(\x+\i*\ns, \y+\j*\ns, \ns, \d-1);
                    };
                };
            };
        };
    };
}
```

## Результат: фрактальная структура

![Ковёр Серпинского, построенный рекурсивным алгоритмом](img/3.1.PNG){#fig:003 width=90%}

# Выводы

## Освоенные технологии и умения

- Программирование графики с использованием `TikZ`
- Построение математических графиков с осями координат
- Создание графов с узлами и рёбрами
- Использование циклов `\foreach` для повторяющихся элементов
- Реализация рекурсивных алгоритмов для фрактальных структур
