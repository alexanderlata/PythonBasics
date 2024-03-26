# Визуализация данных с помощью Python

Для визуализации используйте библиотеки
* Matplotlib
* Plotly
* Seaborn


Для создания массивов используйте библиотеку NumPy

Подключение библиотек
```python
import numpy as np
import matplotlib.pyplot as plt
import plotly.graph_objs as go
import plotly.express as px
import seaborn as sns
```

Чтобы понять как примерно должна выглядеть ваша визуализация вы можете воспользоваться 

* [GeoGebra](https://www.geogebra.org/)
* [Wolfram Alpha](https://www.wolframalpha.com/)
* Microsoft Excel

---

## Упражнение 1 "График функции"

Постройте график данной функции двумя способами: 
1) используя библиотеку Matplotlib; 
2) используя библиотеку Plotly. 

**Обратите внимание** на область определения функции. Функция может иметь выколотые точки или ее можно упростить, при некоторых условиях. 

* $\displaystyle y=x(x+1)(x-1)$
* $\displaystyle y=\frac{x^2-1}{x-1}$
* $\displaystyle y=\frac{x^3-8}{x-2}$

* $\displaystyle y=e^{\frac{1}{x}}$
* $\displaystyle y=\frac{x^4-13x^2+36}{(x-3)(x+2)}$
* $\displaystyle y=\frac{2x}{x^2+1}$
* $\displaystyle y=\frac{x}{x^2-4}$
* $\displaystyle y=\frac{x^3}{2(x+1)^2}$
* $\displaystyle y=\frac{3-2x}{(x-2)^2}$
* $\displaystyle y=\frac{(x-1)^2}{x^2+1}$
* $\displaystyle y=\frac{x^4}{(1+x)^3}$
* $\displaystyle y=\frac{(x-3)^2}{x^2-4x+5}$
* $\displaystyle y=\frac{(x+1)^2}{x^2+2}$
* $\displaystyle y=\frac{x^2-x+1}{3x-x^2-3}$
* $\displaystyle y=x^2-6|x|-2x$
* $\displaystyle y=x^2-|8x+3|$
* $\displaystyle y=\frac{1}{2}\left(\left| \frac{x}{3,5} -\frac{3,5}{x} \right| + \frac{x}{3,5}+\frac{3,5}{x} \right)$
* $\displaystyle y=\sqrt[3]{(x-3)(x-6)^2}$

---

## Упражнение 2 "Фигура ограниченная линиями"

Постройте фигуру, ограниченную линиями

* $\displaystyle y=x^2$ и $\displaystyle y=\frac{x^3}{3}$
* $\displaystyle y=-\frac{1}{2}x^2+3x+6$ и $\displaystyle y=\frac{1}{2}x^2-x+1$
* $\displaystyle y=x^2-6$ и $\displaystyle y=-x^2+5x-6$
* $\displaystyle y=x^2-4x+3$ и $\displaystyle y=3x^2-12x+9$
* $\displaystyle y=\frac{1}{x^2}$, $x=2$, $x=3$ и $y=0$
* $\displaystyle y=4^x$, $y=-x+5$, $x=0$ и $y=0$

---

## Упражнение 3 "Область допустимых решений"

Постройте область решений системы линейных неравенств
 
$$
 \begin{cases}
   4x_1+6x_2 \leqslant 24 
   \\
   3x_1+2x_2\leqslant 12
   \\
   x_1+x_2\leqslant 8
   \\
   x_j\geqslant 0, \, \forall j=1,2.
 \end{cases}
$$
 
$$
\begin{cases}
   4x_1-x_2 \geqslant 0 
   \\
   2x_1+x_2\geqslant 6
   \\
   x_1+2x_2\leqslant 16
   \\
   x_1-x_2\leqslant 0
   \\
   x_1\leqslant 4
   \\
   x_j\geqslant 0, \, \forall j=1,2.
 \end{cases}
$$

$$
\begin{cases}
   5x_1-x_2 \geqslant 0 
   \\
   x_1+x_2 \geqslant 5
   \\
   2x_1-3x_2 \leqslant 0
   \\
   x_2\geqslant 3
   \\
   x_j\geqslant 0, \, \forall j=1,2.
\end{cases}
$$

$$
\begin{cases}
   3x_1-x_2+2 \geqslant 0 
   \\
   2x_1+x_2 \leqslant 16
   \\
   -x_1+2x_2 \geqslant 2
   \\
   x_2\leqslant 6
   \\
   x_1-x_2 \geqslant 3
   \\
   x_j\geqslant 0, \, \forall j=1,2.
\end{cases}
$$

---

## Упражнение 4 "Диаграммы"

Постройте диаграмму (в разработке)

---

## Упражнение 4 "Поверхности и линии уровня"

Постройте поверхности и линии уровня (в разработке)
     
 $x^2-4x+y^2+2=0$

 $x^2+4xy^2+y^2-y-12=0$

 $x^3y+3y^3-x+1=0$

 $(x-1)^2+(y+3)^2=17$

 $x^3+(x-4)y^2=0$

 $x^3+y^2+2x-6=0$

 $y^4-4x^4-6xy=0$

 $xy+\ln y=1$

 $y^2-e^{xy}=1$

 $x^5+y^5-2xy=0$
 