Tutorial
--------

Настоящий раздел объясняет, как использовать базовые операторы в Python.

### Арифметические операторы      

Как и в любых других языках программирования, операторы сложения, вычитания, умножения и деления могут использоваться с числами.<br>

    number = 1 + 2 * 3 / 4.0
    print(number)

Попробуйте посчитать, каким будет ответ. Соблюдает ли python порядок действий?

Другим доступным оператором является оператор по модулю (%), который возвращает целочисленный остаток от деления. делимое % делитель = остаток.

    remainder = 11 % 3
    print(remainder)

Использование двух символов умножения дает степенное соотношение.

    squared = 7 ** 2
    cubed = 2 ** 3
    print(squared)
    print(cubed)

### Использование операторов со строками

Python поддерживает объединение строк с помощью оператора сложения:

    helloworld = "hello" + " " + "world"
    print(helloworld)

Python также поддерживает умножение строк для формирования строки с повторяющейся последовательностью:

    lotsofhellos = "hello" * 10
    print(lotsofhellos)

### Использование операторов со списками

Списки могут объедииться с помощью операторов сложения:

    even_numbers = [2,4,6,8]
    odd_numbers = [1,3,5,7]
    all_numbers = odd_numbers + even_numbers
    print(all_numbers)

Как и в строках, Python поддерживает формирование новых списков с повторяющейся последовательностью, используя оператор умножения:

    print([1,2,3] * 3)

Упражнение
--------

Цель этого упражнения - создать два списка с именами `x_list` и `y_list`,
Вам также необходимо создать список с именем big_list, который содержит переменные x и y, по 10 экземпляров каждой, объединяя два созданных Вами списка.
Вам также необходимо создать список с именем big_list, который содержит переменные  `x` и `y`, по 10 раз каждой, объединяя два созданных Вами списка.

Tutorial Code
-------------

x = object()
y = object()

# TODO: change this code
x_list = [x]
y_list = [y]
big_list = []

print("x_list contains %d objects" % len(x_list))
print("y_list contains %d objects" % len(y_list))
print("big_list contains %d objects" % len(big_list))

# testing code
if x_list.count(x) == 10 and y_list.count(y) == 10:
    print("Almost there...")
if big_list.count(x) == 10 and big_list.count(y) == 10:
    print("Great!")

Expected Output
---------------

Ex().check_object('x_list').has_equal_value(expr_code = 'len(x_list)')
Ex().check_object('y_list').has_equal_value(expr_code = 'len(y_list)')
Ex().check_object('big_list').has_equal_value(expr_code = 'len(big_list)')
success_msg('Good work!')

Solution
--------

x = object()
y = object()

# TODO: change this code
x_list = [x] * 10
y_list = [y] * 10
big_list = x_list + y_list

print("x_list contains %d objects" % len(x_list))
print("y_list contains %d objects" % len(y_list))
print("big_list contains %d objects" % len(big_list))

# testing code
if x_list.count(x) == 10 and y_list.count(y) == 10:
    print("Almost there...")
if big_list.count(x) == 10 and big_list.count(y) == 10:
    print("Great!")
