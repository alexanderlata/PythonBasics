# Визуализация данных с помощью Python

Для визуализации используйте библиотеки
* Matplotlib
* Plotly
* Seaborn


Для создания массивов используйте библиотеку NumPy
Для работы с таблицами используйте библиотеку Pandas

Подключение библиотек
```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import plotly.graph_objs as go
import plotly.express as px
import seaborn as sns
```

Чтобы понять как примерно должна выглядеть ваша визуализация вы можете воспользоваться 

* [GeoGebra](https://www.geogebra.org/)
* [Wolfram Alpha](https://www.wolframalpha.com/)
* Microsoft Excel

Примеры визуализаций 
* https://python-graph-gallery.com/barplot/

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

* Постройте круговую диаграмму, отражающую соотношение притока воды в Ладожское озеро из разных источников.

| Река     | Приток воды |
| -------- | ----------- |
| Свирь    |     785     |
| Вуокса   |     684     |
| Волхов   |     593     |
| Сясь     |      53     |
| Янисйоки |     45.5    |
| Олонка   |      35     |

```python
influx = [785, 684, 593, 53, 45.5, 35]
river = ['Свирь', 'Вуокса', 'Волхов', 'Сясь', 'Янисйоки', 'Олонка']
```
* В таблице приведены данные о выработке электроэнергии в России с 1998 г. по 2006 г. в миллиардах киловатт-часов (млрд. кВт*ч).
```python
data = pd.DataFrame({'Год': [1998, 1999, 2000, 2001, 2002, 2003, 2004, 2005, 2006], 
                     'Электроэнергия': [827, 846, 878, 891, 891, 915, 931, 953, 991] })
```
Постройте столбиковую диаграмму по данным таблицы.

* В таблице приведены значения роста и веса 15 юношей (рост в см; вес в кг).
```python
data = pd.DataFrame({'Рост': [167, 169, 179, 178, 177, 175, 171, 181, 174, 175, 180, 174, 172, 178, 171], 
                     'Вес': [62, 67, 70, 72, 70, 69, 63, 80, 73, 66, 75, 70, 67, 74, 66] })
```
Постройте диаграмму рассеивания. Есть ли взаимосвязь между ростом и весом юношей?

* В таблице приведены данные о весе и росте 12 девушек (рост в см; вес в кг).
```python
data = pd.DataFrame({'Рост': [165, 177, 161, 162, 170, 176, 177, 164, 166, 161, 169, 159], 
                     'Вес': [53, 67, 45, 53, 60, 62, 58, 60, 62, 55, 55, 49] })
```
Постройте диаграмму рассеивания. Есть ли взаимосвязь между ростом и весом девушек?

---

## Упражнение 4 "Поверхности и линии уровня"

Постройте на одном рисунке (Figure) на разных областях (Axes) график функции двух переменных (поверхность) $z=f(x,y)$ и линию уровня, удовлетворяющую уравнению $f(x,y)=a$.
     
* $f(x,y)=x^2-4x+y^2+2, \quad a=0$

* $f(x,y)=x^2+4xy^2+y^2-y-12, \quad a=0$

* $f(x,y)=x^3y+3y^3-x+1, \quad a=0$

* $f(x,y)=(x-1)^2+(y+3)^2, \quad a=17$

* $f(x,y)=x^3+(x-4)y^2, \quad a=0$

* $f(x,y)=x^3+y^2+2x-6, \quad a=0$

* $f(x,y)=y^4-4x^4-6xy, \quad a=0$

* $f(x,y)=xy+\ln y, \quad a=1$

* $f(x,y)=y^2-e^{xy}, \quad a=1$

* $f(x,y)=x^5+y^5-2xy, \quad a=0$
 