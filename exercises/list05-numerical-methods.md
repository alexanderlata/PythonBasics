# Численные методы в Python

* Для создания матриц используйте массивы из библиотеки `NumPy`
* Для визуализации используйте библиотеку `Matplotlib`
* Для поиска локального минимума (максимума) на отрезке используйте метод `minimize_scalar` библиотеки `scipy.optimize`

```python
# Подключение библиотек
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from scipy.optimize import minimize_scalar
```

__Замечания__

* Библиотека NumPy: При использовании функции `numpy.linalg.solve` для решения системы уравнений с помощью LU-разложения или QR-разложения, если система не имеет решения или имеет бесконечно много решений, библиотека NumPy выдаст ошибку типа `LinAlgError`.
* Для численного вычисления определенного интеграла в Python с использованием библиотеки NumPy можно воспользоваться функцией `numpy.trapz` для метода трапеций.

---

## Упражнение 1 "Действия над матрицами"

* Даны матрицы 

$$
A=\begin{pmatrix}
1 & -2 & 1 \\
0 & 0 & 1 \\
0 & 1 & 1
\end{pmatrix},  
B=\begin{pmatrix}
-1 & 2 \\
-1 & 0 \\
3 & 1
\end{pmatrix} \text{ и } C=\begin{pmatrix}
2 & -1 \\
-2 & 1
\end{pmatrix}.
$$ 

Какие из этих матриц можно перемножить друг на друга?
Найдите соответствующие произведения.

* Даны матрицы  

$$
\begin{aligned}
A=\begin{pmatrix}
3 & 2 & 1 \\
0 & 4 & 3
\end{pmatrix}, 
B=\begin{pmatrix}
1 & 1 \\
-2 & 2 
\end{pmatrix} \text{ и } C=\begin{pmatrix}
3 & -3 & 1 \\
0 & 0 & 2 \\
-1 & 1 & 0
\end{pmatrix}.
\end{aligned}
$$ 

Какие из этих матриц можно перемножить друг на друга?
Найдите соответствующие произведения.

* Даны матрицы 

$$
\begin{aligned}
A=\begin{pmatrix}
1 & -3 & 5 \\ 
2 & 4 & 7
\end{pmatrix} \text{ и } B=\begin{pmatrix}
4 & -3 \\
6 & 5 \\ 
1 & -1
\end{pmatrix}.
\end{aligned}
$$ 

Вычислите матрицу $C=3A-2B^{\rm T}$.

* Даны матрицы 

$$
\begin{aligned}
A=
\begin{pmatrix}
1 & 0 & 3 \\ 
2 & 4 & 1 \\
1 & -4 & 2
\end{pmatrix}, 
B=
\begin{pmatrix}
1 \\
3 \\ 
2 
\end{pmatrix}, 
C=
\begin{pmatrix}
-1 \\
2 \\ 
1 
\end{pmatrix}.
\end{aligned}
$$ 

Вычислите матрицу $D=A^{\rm T}B+2C$.

---

## Упражнение 2 "Системы линейных уравнений"

Решите систему линейных уравнений тремя способами: 
а) методом `numpy.linalg.solve`
б) методом Крамера (реализуйте метод самостоятельно)
в) методом обратной матрицы (реализуйте метод самостоятельно)

* 
$$
\begin{cases}
 3x_1+4x_2+6x_3=2, \\
 2x_1+3x_2-5x_3=-1, \\
 5x_1+7x_2+2x_3=1.
\end{cases}
$$

* 
$$
\begin{cases}
 4x_1-5x_2-3x_3+1=0, \\
 3x_1-x_2-2x_3+2=0, \\
 5x_1+x_2-3x_3+3=0.
\end{cases}
$$

* 
$$
\begin{cases}
  2x_1+2x_2+x_3+2x_4=1, \\
  3x_1+x_2-x_3+2x_4=-1,  \\
  4x_1+3x_2+2x_3+3x_4=5,  \\
  2x_1-x_2+2x_3-7x_4=19.
\end{cases}
$$

---

## Упражнение 3 "Экстремум функции одной переменной"

Используя метод `minimize_scalar` библиотеки `scipy.optimize` выясните имеет ли функция $f(x)$ на отрезке $[-7, 7]$ экстремумы.

* $\displaystyle y=x(x+1)(x-1)$
* $\displaystyle y=\frac{x^2-1}{x-1}$
* $\displaystyle y=\frac{x^3-8}{x-2}$

* $\displaystyle y=e^{\frac{1}{x}}$
* $\displaystyle y=\frac{x^4-13x^2+36}{(x-3)(x+2)}$


__Замечание__: Последовательность шагов следующая
* Постройте график функции $f(x)$ 
* Если функция на отрезке $[a, b]$ имеет несколько экстремумов или точки разрыва, то разбейте отрезок $[a, b]$ на отрезки меньшей длины и найдите экстремумы на них
* Для нахождения максимума функции $f(x)$, ее необходимо умножить на $-1$ и исследовать новую функцию на минимум

---

## Упражнение 4 "Интеграл Римана"

Используя метод `trapz` (метод трапеций) библиотеки `numpy` вычислите численно интеграл Ньютона ("определенный интеграл")
* $\displaystyle \int\limits_{1}^{2}\left(3x-2\right)^3 dx$
* $\displaystyle \int\limits_{-1}^{2}x(3x^4-4x^2+1) dx$
* $\displaystyle \int\limits_{\frac{1}{2}}^{1}\left(2x-1\right)^7 dx$
* $\displaystyle \int\limits_{0}^{1}\sqrt{1+x} dx$
* $\displaystyle \int\limits_{0}^{1}\left(e^x+1\right)^4 e^x dx$
* $\displaystyle \int\limits_{1}^{2}\frac{3x dx}{\sqrt{5-x^2}}$
* $\displaystyle \int\limits_{0}^{1}\frac{x dx}{(x^2+1)^2}$
* $\displaystyle \int\limits_{-2\sqrt{3}}^{2}\frac{dx}{(4+x^2)^2}$
* $\displaystyle \int\limits_{0}^{2\pi}\sin^4{x} dx$
* $\displaystyle \int\limits_{1}^{2}\frac{e^{\frac{1}{x}} dx}{x^2}$
* $\displaystyle \int\limits_{\frac{\pi}{6}}^{\frac{\pi}{2}}e^{\sin{x}}\cos{x} dx$
* $\displaystyle \int\limits_{e}^{e^3}\frac{\ln^2{x}}{\frac{1}{x}} dx$
* $\displaystyle \int\limits_{0}^{\frac{\pi}{3}}\frac{\sin{x}}{\cos^3{x}} dx$
* $\displaystyle \int\limits_{1}^{e}\cos(\ln{x}) dx$

---