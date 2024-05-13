# Символьные вычисления в Python

Для символьных вычислений используйте библиотеку `SymPy`

Подключение библиотек
```python
import sympy as sp # мы импортировали все данные из библиотеки в переменную sp
from sympy import * # знак звездочки означает, что мы импортировали все данные из библиотеки в текущее пространсво имен
```
---

<div class="alert alert-block alert-warning">
<b>Внимание:</b> SymPy не всегда упрошает выражения до самого простого.
</div>

____

## Упражнение 1 "Выражение"

* Вычислите значение выражения $(a+4 \cdot b) \cdot (a-3 \cdot b)+a^2$ при $a=7$ и $b=15$. 
* Вычислите значение выражения $\displaystyle \frac{11a^6b^3-(3a^2b)^3}{4a^2b^6}$ при $b=2$.
* Вычислите значение выражения $\sqrt{a^3+b^3}+\sqrt[3]{a^2+ab+b^2}$ при $a=7$ и $b=15$.
* Вычислите значение выражения $\displaystyle \frac{\left(\sqrt{13} + \sqrt{7}\right)^2}{10 + \sqrt{91}}$.
* Вычислите значение выражения $\displaystyle \frac{g(2-x)}{g(2+x)}$, если $g(x)=\sqrt[3]{x(4-x)}$.

**Подсказка:** используйте методы `subs`, `Rational` и `simplify`.

---

## Упражнение 2 "Рациональные функции"

Разложите рациональную дробь в сумму простейших дробей над $\mathbb{R}$

* $\displaystyle \frac{2x^2-5}{x^4-5x^2+6}$
* $\displaystyle \frac{x^5+x^4-8}{x^3-4x}$
* $\displaystyle \frac{x^6-2x^4+3x^3-9x^2+4}{x^5-5x^3+4x}$
* $\displaystyle \frac{7x^3-9}{x^4-5x^3+6x^2}$
* $\displaystyle \frac{x^3-2x^2+4}{x^3(x-2)^2}$
* $\displaystyle \frac{x^3-2x^2+4}{x^3(x-2)^2}$
* $\displaystyle \frac{3x^2+1}{\left(x^2-1\right)^3}$
* $\displaystyle \frac{3x^2+x+3}{(x-1)^3\left(x^2+1\right)}$
* $\displaystyle \frac{x^5+2x^3+4x+4}{x^4+2x^3+2x^2}$

* $\displaystyle \frac{x^3-6}{x^4+6x^2+8}$
* $\displaystyle \frac{1}{1+x^4}$
* $\displaystyle \frac{x^3+x-1}{\left(x^2+2\right)^2}$
* $\displaystyle \frac{1}{x(4+x^2)^2(1+x^2)}$

**Подсказка:** используйте метод `apart`.

---

## Упражнение 2 "Уравнения и системы уравнений"

* Решите уравнение
* Решите систему уравнений методом Гаусса

**Подсказка:** используйте методы `solve`, `Matrix` и `rref`.

---


## Упражнение 4 "Ряд Тейлора"

Разложите функцию в ряд Тейлора по степеням переменной $x$ до члена $x^{10}$ __включительно__

* $f(x) = \sin 3x$
* $f(x) = \cos 4x$
* $f(x) = \tg 5x$
* $f(x) = \ctg 7x$
* $f(x) = e ^{3x}$
* $\displaystyle f(x) = \frac{1}{x-1}$
* $f(x) = \ln(x-1)$


**Подсказка:** используйте метод `series`.

---

## Упражнение 5 "Пределы"

Вычислите предел функции

* $\displaystyle \lim_{x\to\pm\infty} \frac{4x^3+2x+3}{2+x+5x^2}$

* $\displaystyle \lim_{x\to\pm\infty} \frac{x^3+1}{2+3x+5x^3}$

* $\displaystyle \lim_{x\to\pm\infty} \frac{4x^2-2x+3}{x^3+5x^4}$

* $\displaystyle \lim_{x\to\pm\infty} \frac{3x-5x^2+2}{2x^3+x+3}$

* $\displaystyle \lim_{x\to\pm\infty} \frac{x^4-5x^2+x}{2+x^3}$

* $\displaystyle \lim_{x\to 1 - \text{o}} \frac{x^3-x}{x^2-2x+1}$
* $\displaystyle \lim_{x\to -2 + \text{o}} \frac{2x^2-x-10}{x^3-x^4+24}$
* $\displaystyle \lim_{x\to 1} \frac{x^2-3x+2}{x^2+x-6}$
* $\displaystyle \lim_{x\to -2 + \text{o}} \frac{x^2-3x+2}{x^2+x-6}$
* $\displaystyle \lim_{x\to 2 - \text{o}} \frac{\sqrt{x^2+5}-3}{x-2}$
* $\displaystyle \lim_{x\to 3} \frac{\sqrt{x+6}-3}{x-3}$
* $\displaystyle \lim_{x\to +\infty} \left(\sqrt{x^2+2}-x \right)$
* $\displaystyle \lim_{x\to -\infty} \left(\sqrt{x^2+2}-x \right)$
* $\displaystyle \lim_{x\rightarrow 0} \frac{\arcsin\frac{x}{2}}{\arctg 4x}$
* $\displaystyle \lim_{x\rightarrow 0} \frac{\sin 9x - \sin 3x}{3x\cos 5x}$
* $\displaystyle \lim_{x\rightarrow 0} \frac{\sin 4x - \sin 2x}{x\cos 6x}$
* $\displaystyle \lim_{x\rightarrow 0} \frac{\sqrt{x+9}-3}{\sin\frac{x}{3}}$
* $\displaystyle \lim_{x\rightarrow 0} \frac{\sin x}{\sqrt{9-x}-3}$
* $\displaystyle \lim_{x\rightarrow \infty} \left(\frac{4x}{4x+5}\right)^{x+1}$
* $\displaystyle \lim_{x\rightarrow \infty} \left(\frac{5-2x}{3-2x}\right)^{4x-5}$
* $\displaystyle \lim_{x\rightarrow \infty} \left(\frac{2-3x}{1-3x}\right)^{5x+2}$
* $\displaystyle \lim_{x\rightarrow 0} \left(1-3x\right)^{\frac{2}{x}}$
* $\displaystyle \lim_{x\rightarrow 0} \left(1+2x\right)^{\frac{4}{x}}$
* $\displaystyle \lim_{x\rightarrow 0} \left(\frac{2}{2+x}\right)^{\frac{1}{3x}}$

**Подсказка:** используйте метод `limit`.

---


## Упражнение 6 "Производные"

Вычислите все частные производные первого и второго порядков от данных функций

* $u = 4\ln\left(3+x^2\right)-8xyz$
* $\displaystyle u = \frac{1}{4}x^2y-\sqrt{x^2+5z^2}$
* $u = xz^2-\sqrt[3]{x^2y}$
* $u = \sin\left(x+2y\right)+\sqrt{xyz}$
* $u = x^2y^2z-\ln\left(z-x\right)$
* $u = \ln\left(x+\sqrt{y^2+z^2}\right)$
* $u = \arctg\sqrt{x-y}$
* $\displaystyle u = \frac{\sqrt{x}}{y}-\frac{yz}{x+\sqrt{y}}$
* $\displaystyle u = ye^{\tg(x-2y)}$
* $\displaystyle u = \ln\frac{\tg3y}{x+y}$
* $\displaystyle u = e^{x^2-y}\tg(x-y^2)$
* $\displaystyle u = \frac{\sqrt[3]{xy}}{\sqrt[3]{x}+\sqrt[3]{y}}$
* $\displaystyle u = \frac{e^{-3y}}{5x-y}$
* $\displaystyle u = \frac{\ctg2x}{\sqrt{y^3-3}}$
* $\displaystyle u = 5^{x\ln y}+\arcsin(y^2+1)$
* $\displaystyle u = 3^{2y+3}\tg x$
* $\displaystyle u = \frac{\arctg\sqrt{x-1}}{2y+3}$
* $\displaystyle u = x^y + y^x$
* $\displaystyle u = (2x+3y)^{x+y}$
* $\displaystyle u = (2x+3y)^{\sin xy}$
* $\displaystyle u = x^{3y}+3^{x^y}+x^{y^3}$
* $\displaystyle u = (2y-1)^{\ln 3x}$
* $\displaystyle u = (2y-x)^{\ln(x+y)}$
* $\displaystyle u = \left(\cos 5x\right)^{\tg(x-y)}$

**Подсказка:** используйте метод `diff`.

---

## Упражнение 7 "Дифференциальные уравнения"

Покажите, что данная функция удовлетворяет данному дифференциальному уравнению

|Функция|Уравнение|
|-|-|
|$z = x^3 - xy^2 + y^3$|$x \cdot z^{\prime}_x + y \cdot z^{\prime}_y = 3z$|
|$\displaystyle z = \frac{x^2-y^2}{x^2+y^2}$|$x \cdot z^{\prime}_x + y \cdot z^{\prime}_y = 0$|
|$\displaystyle z = \sqrt[3]{x^4+5y^4}$|$\displaystyle x \cdot z^{\prime}_x + y \cdot z^{\prime}_y = \frac{4}{3} z$|
|$\displaystyle z = x \ln \frac{y}{x}$|$x \cdot z^{\prime}_x + y \cdot z^{\prime}_y = z$|
|$z = e^{xy}$|$x^2 \cdot z^{\prime\prime}_{xx} + y^2 \cdot z^{\prime\prime}_{yy} =0$|
|$\displaystyle z = y\sqrt{\frac{y}{x}}$|$x^2 \cdot z^{\prime\prime}_{xx} + y^2 \cdot z^{\prime\prime}_{yy} =0$|

**Подсказка:** вычислите производные и сделайте проверку.

---

## Упражнение 8 "Интегралы"

Вычислите интеграл Ньютона

* $\displaystyle \int{\frac{dx}{x^2+4x+5}}$
* $\displaystyle \int{\frac{x^2+4x-2}{x^2+3x-4}}dx$
* $\displaystyle \int{\frac{dx}{\sqrt{9x^2+6x-1}}}$
* $\displaystyle \int{\frac{x+3}{\sqrt{3+4x-4x^2}}}dx$
* $\displaystyle \int{\sqrt{3+2x-x^2}}dx$
* $\displaystyle \int{x}\sin{2x}dx$
* $\displaystyle \int{x}\cos{x}dx$
* $\displaystyle \int{\frac{xdx}{\sin^2{x}}}$
* $\displaystyle \int{x} \cdot 3^xdx$
* $\displaystyle \int{x}^3\ln{x}dx$
* $\displaystyle \int\arccos{x}dx$	 
* $\displaystyle \int\arctg\sqrt{x}dx$
* $\displaystyle \int\frac{\arcsin{x}}{\sqrt{x+1}}dx$
* $\displaystyle \int{x}\tg^2xdx$
* $\displaystyle \int\frac{\lg{x}}{x^3}dx$
* $\displaystyle \int\ln\left(x^2+1\right)dx$
* $\displaystyle \int\frac{x^2dx}{\left(1+x^2\right)^2}$
* $\displaystyle \int\frac{x^3dx}{\sqrt{1+x^2}}$
* $\displaystyle \int{e^x\sin{x}}dx$
* $\displaystyle \int{\frac{\left(2x^2-5\right)dx}{x^4-5x^2+6}}$
* $\displaystyle \int{\frac{x^5+x^4-8}{x^3-4x}}dx$
* $\displaystyle \int{\frac{x^6-2x^4+3x^3-9x^2+4}{x^5-5x^3+4x}}dx$
* $\displaystyle \int{\frac{\left(7x^3-9\right)dx}{x^4-5x^3+6x^2}}$
* $\displaystyle \int{\frac{x^3-2x^2+4}{x^3(x-2)^2}}dx$	
* $\displaystyle \int{\frac{x^3-2x^2+4}{x^3(x-2)^2}}dx$
* $\displaystyle \int{\frac{3x^2+1}{\left(x^2-1\right)^3}}dx$
* $\displaystyle \int{\frac{\left(3x^2+x+3\right)dx}{(x-1)^3\left(x^2+1\right)}}$	
* $\displaystyle \int{\frac{x^5+2x^3+4x+4}{x^4+2x^3+2x^2}}dx$	 
* $\displaystyle \int{\frac{\left(x^3-6\right)dx}{x^4+6x^2+8}}$	
* $\displaystyle \int{\frac{dx}{1+x^4}}$
* $\displaystyle \int{\frac{x^3+x-1}{\left(x^2+2\right)^2}}dx$
* $\displaystyle \int{\frac{dx}{x(4+x^2)^2(1+x^2)}}$

**Подсказка:** используйте метод `integrate`.

---