---
## Front matter
lang: ru-RU
title: Презентация по лабораторной работе №4
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

Целочисленная арифметика многократной точности является фундаментом криптографических алгоритмов и систем защиты информации, где стандартные типы данных недостаточны для работы с большими числами.

## Объект и предмет исследования

- Алгоритмы многоточной целочисленной арифметики
- Операции сложения, вычитания, умножения и деления
- Язык программирования Julia

## Цели и задачи

Ознакомиться с целочисленной арифметикой многократной точности и реализовать рассмотренные алгоритмы программно на языке Julia.

## Материалы и методы

- Язык программирования Julia
- Концепции модульной арифметики
- Алгоритмы работы с многоразрядными числами

# Результаты

## Алгоритм 1: сложение неотрицательных целых чисел
```julia
function add_large_integers(u::Vector{Int}, v::Vector{Int}, b::Int)
    n = length(u)
    w = zeros(Int, n + 1)
    k = 0
    for j in n:-1:1
        digit_sum = u[j] + v[j] + k
        w[j + 1] = digit_sum % b
        k = digit_sum ÷ b
    end
    w[1] = k
    return w
end
```

## Алгоритм 2: вычитание неотрицательных целых чисел
```julia
function subtract_large_integers(u::Vector{Int}, v::Vector{Int}, b::Int)
    n = length(u)
    w = zeros(Int, n)
    k = 0
    for j in n:-1:1
        digit_diff = u[j] - v[j] + k
        if digit_diff < 0
            digit_diff += b
            k = -1
        else
            k = 0
        end
        w[j] = digit_diff
    end
    return w
end
```

## Алгоритм 3: умножение неотрицательных целых чисел
```julia
function multiply_large_integers(u::Vector{Int}, v::Vector{Int}, b::Int)
    n = length(u)
    m = length(v)
    w = zeros(Int, n + m)
    for j in m:-1:1
        if v[j] == 0; continue; end
        k = 0
        for i in n:-1:1
            t = u[i] * v[j] + w[i + j] + k
            w[i + j] = t % b
            k = t ÷ b
        end
        w[j] = k
    end
    return w
end
```

## Алгоритм 4: быстрый столбик
```julia
function fast_column_multiply(u::Vector{Int}, v::Vector{Int}, b::Int)
    n = length(u)
    m = length(v)
    w = zeros(Int, n + m)
    for s in 0:(m + n - 2)
        t = 0
        for i in 0:s
            if n - i > 0 && m - (s - i) > 0
                t += u[n - i] * v[m - (s - i)]
            end
        end
        w[m + n - 1 - s] = t % b
        t = t ÷ b
    end
    w[1] = t
    return w
end
```

## Алгоритм 5: деление многоразрядных целых чисел
```julia
function divide_large_integers(u::Vector{Int}, v::Vector{Int}, b::Int)
    n = length(u) - 1
    t = length(v) - 1
    q = zeros(Int, n - t + 1)
    r = copy(u)
    while compare_large_integers(r, v, n - t, b) >= 0
        q[end] += 1
        r = subtract_scaled(r, v, n - t, b)
    end
    for i in n:-1:(t + 1)
        q[i-t-1] = r[i+1] >= v[t+1] ? b - 1 : (r[i+1] * b + r[i]) ÷ v[t+1]
        r = subtract_scaled(r, v, i - t - 1, b, q[i - t - 1])
        if r[1] < 0
            r = add_scaled(r, v, i - t - 1, b)
            q[i - t - 1] -= 1
        end
    end
    return q, r
end
```

# Выводы

## Освоенные технологии и умения

- Реализация алгоритмов многоточной целочисленной арифметики на Julia
- Работа с операциями сложения, вычитания, умножения и деления больших чисел
- Применение принципов модульной арифметики
- Управление переносами, заимствованиями и промежуточными результатами
- Разработка надёжных решений для вычислений в произвольной системе счисления
