# Функции и их особенности в Python

## Синтаксис создания функции

Для создания функции используется ключевое слово `def`, после которого указывается имя функции и список параметров в круглых скобках. Если их нет, то скобки остаются пустыми, но они обязательно должны быть. Далее идет двоеточие, обозначающее окончание заголовка функции. Тело функции выделяется так же, как тело условия или цикла: **четырьмя пробелами**. 

---

Синтаксис 

```python
def <имя функции>([<параметры функции>]):
    <тело функции>
    [return <возвращаемый результат>]
```
При объявлении (задании) функции в квадратные скобки заключены необязательные элементы.

---

Возврат значения функцией осуществляется с помощью оператора `return`, после которого указывается возвращаемое значение.

**Обратите внимание**: функция в Python всегда возвращает результат, даже если в ней нет `return` или присутствует `return` без возвращаемого значения. Тогда возвращаемый результат будет `None` — специальный тип данных в Python, который дословно можно перевести с английского как «ничего». 

---

## Упражнение 1
**Функции с позиционными аргументами**

* Напишите функцию, принимающую 1 аргумент – натуральное число $n$ - и возвращающую 1 значение: сумму натуральных чисел от 1 до $n$. При этом нельзя использовать встроенную функцию `sum()`.

* Напишите функцию, принимающую 1 аргумент – натуральное число $n$ - и возвращающую 1 значение: факториал числа $n$. При этом нельзя использовать `math.factorial()`.

* Напишите функцию, принимающую 1 аргумент - натуральное число $n$ – и возвращающую 1 значение: число Фибоначчи с номером $n$.

* Напишите функцию, принимающую 1 аргумент – сторону квадрата – и возвращающую 3 значения (с помощью кортежа): периметр квадрата, площадь квадрата и диагональ квадрата.

* Напишите функцию, принимающую 2 позиционных аргумента $n$ и $d$: первый $n$ - номер члена арифметической прогрессии ($n$ натуральное число), второй $d$ - разность арифметической прогрессии,  - и возвращающую 1 значение: $n$-ый член арифметической прогрессии.

* Напишите функцию, принимающую 2 позиционных аргумента $n$ и $q$: первый $n$ - номер члена геометрической прогрессии ($n$ натуральное число), второй $q$ - знаменатель геометрической прогрессии - и возвращающую 1 значение: $n$-ый член геометрической прогрессии.

* Напишите функцию, принимающую 3 позиционных аргумента: первые два – числа, третий – операция, которая должна быть произведена над ними. Если третий аргумент `+`, сложить их; если `-`, то вычесть (из первого второе); `*` - умножить; `/` - разделить (первое на второе). В остальных случаях вернуть строку «Неизвестная операция».

* Пользователь делает вклад в размере $a$ рублей сроком на $years$ лет под 10\% годовых (каждый год размер его вклада увеличивается на 10\%. Эти деньги прибавляются к сумме вклада, и на них в следующем году тоже будут проценты). Напишите функцию, принимающую аргументы $a$ и $years$ и возвращающую сумму, которая будет на счету пользователя.

---

## Упражнение 2
**Функции с именованными аргументами**

* Напишите функцию, принимающую 2 аргумента $n$ и $d$: первый $n$ - номер члена арифметической прогрессии ($n$ натуральное число), второй $d$ - разность арифметической прогрессии,  - и возвращающую 1 значение: сумму $n$ первых членов арифметической прогрессии. По умолчанию $d=1$

* Напишите функцию, принимающую 2 позиционных аргумента $n$ и $q$: первый $n$ - номер члена геометрической прогрессии ($n$ натуральное число), второй $q$ - знаменатель геометрической прогрессии - и возвращающую 1 значение: сумму $n$ первых членов геометрической прогрессии. По умолчанию $q=1$

* Напишите функцию, которая вычисляет значение многочлена пятой степени $p(x)=a_0x^5+a_1x^4+a_2x^3+a_3x^2+a_4x+a_5$ с действительными коэффициентами. По умолчанию $a_i = 1$ для всех $i$. Сколько параметров нужно задать при объявлении функции?

* Напишите функцию, которая начисляет новогодние премии сотрудникам. Эта функция:
    - имеет два аргумента по умолчанию – `salary=120000` и `bonus=10` (оклад и премия);
    - получает два позиционных аргумента `name` и `last_name` – имя и фамилию сотрудника;
    - учитывает индивидуальные оклад и премию (см. примеры вызова);
    - выводит размер новогодней премии для сотрудника и зарплату с учетом премии.
    
    **Примеры вызова функции**:
    ```python
    ny_bonus('Алина', 'Тимофеева', salary=150000, bonus=25)
    ny_bonus('Алексей', 'Ковалев', bonus=15)
    ny_bonus('Игорь', 'Ефимов')
    ny_bonus('Анастасия', 'Яковлева', salary=100000, bonus=20) 
    ``` 

    **Вывод**:
    ```
    Новогодняя премия сотрудника Алина Тимофеева: 37500.00 руб.
    Оклад: 150000.00 руб.
    Всего к выдаче: 187500.00 руб.

    Новогодняя премия сотрудника Алексей Ковалев: 18000.00 руб.
    Оклад: 120000.00 руб.
    Всего к выдаче: 138000.00 руб.

    Новогодняя премия сотрудника Игорь Ефимов: 12000.00 руб.
    Оклад: 120000.00 руб.
    Всего к выдаче: 132000.00 руб.

    Новогодняя премия сотрудника Анастасия Яковлева: 20000.00 руб.
    Оклад: 100000.00 руб.
    Всего к выдаче: 120000.00 руб.
    ```

---

## Упражнение 3
**Функции с переменным числом аргументов**

* Напишите функцию `arith_mean`, которая принимает произвольное количество целых чисел (позиционных аргументов), и возвращает среднее арифметическое без использования встроенных функции `sum()` и `len()`.

* Напишите функцию sq_sum(), которая принимает произвольное количество числовых аргументов и возвращает сумму их квадратов.

* Напишите функцию, которая принимает произвольное количество строк (позиционных аргументов), и преобразует каждое слово в верхний регистр. **Подсказка**: используйте `upper()`.

---

## Упражнение 4
**Лямбда-функции в pandas**

При объявлении лямбда-функции указывается ключевое слово `lambda`, затем перечисляются аргументы функции, затем двоеточие и пробел, а далее указывается возвращаемое функцией значение (`return` не используется).

Синтаксически при объявлении Лямбда-функции записываются в одну строку. 

```python
import pandas as pd

# Создадим датафрейм с новыми данными 
new_data = pd.DataFrame({'age': [31,44,30,64], 
                         'male': [1,1,0,1], 
                         'marr': [0,1,1,1], 
                         'totwrk': [5020,2815,3786,2580], 
                         'sleep': [2920,2670,3083,3448] })
# age - возраст (в годах)
# male - гендерный фактор (бинарная, 1 если мужчина)
# marr - семейный статус (бинарная, 1 если женат/заужем)
# totwrk - занятость (мин/нед) 
# sleep - продолжительность сна (мин/нед)
# tasks - количество выполненных задач (шт/нед)

new_data

```

* Создайте новый столбец `bonus` и заполните его по правилу: если количество выполненных задач в неделю больше 15, то назначить сотруднику премию

---