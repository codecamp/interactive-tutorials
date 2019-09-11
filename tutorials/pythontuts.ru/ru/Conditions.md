Tutorial
--------

Python использует логические переменные для оценки условий. Логические значения True и False возвращаются при сравнении или оценке выражения. Например:

    x = 2
    print(x == 2) # prints out True
    print(x == 3) # prints out False
    print(x < 3) # prints out True

Обратите внимание, что присвоение переменной выполняется с помощью одного оператора равенства "=", тогда как сравнение между двумя переменными выполняется с помощью оператора двойного равенства "==". Оператор "не равно" помечен как "!=".

### Булевы операторы

Логические операторы "and" и "or" позволяют создавать сложные логические выражения, например:

    name = "John"
    age = 23
    if name == "John" and age == 23:
        print("Your name is John, and you are also 23 years old.")

    if name == "John" or name == "Rick":
        print("Your name is either John or Rick.")

### Оператор "in"

Оператор "in" может быть использован для проверки, существует ли указанный объект в итерируемом контейнере объекта, таком как список:

    name = "John"
    if name in ["John", "Rick"]:
        print("Your name is either John or Rick.")

Python использует отступы для определения блоков кода вместо скобок. Стандартный отступ Python - это 4 пробела, хотя табуляция и любой другой размер пробела будут работать, если они единообразны. Обратите внимание, что кодовые блоки не нуждаются в завершении.

Вот пример использования оператора if в Python с использованием блоков кода:

    statement = False
    another_statement = True
    if statement is true:
        # do something
        pass
    elif another_statement is true: # else if
        # do something else
        pass
    else:
        # do another thing
        pass

Например:

    x = 2
    if x == 2:
        print("x equals two!")
    else:
        print("x does not equal to two.")

Утверждение оценивается как истинное, если является правильным одно из следующих утверждений:
1. Логическая переменная "True" задается или вычисляется с использованием выражения, такого как арифметическое сравнение.
2. Объект, который не считается "пустым", пропускается.

Вот несколько примеров для объектов, которые рассматриваются как пустые:
1. An empty string: ""
2. An empty list: []
3. The number zero: 0
4. The false boolean variable: False

### Оператор "is"

В отличие от оператора двойного равенства "==", оператор "is" соответствует не значениям переменных, а самим экземплярам. Например:

    x = [1,2,3]
    y = [1,2,3]
    print(x == y) # Prints out True
    print(x is y) # Prints out False

### Оператор "not"

Использование "not" перед логическим выражением инвертирует его:

    print(not False) # Prints out True
    print((not False) == (False)) # Prints out False

Упражнение
--------

Измените переменные в первом разделе, чтобы каждый оператор if разрешался как True.

Tutorial Code
-------------

# change this code
number = 10
second_number = 10
first_array = []
second_array = [1,2,3]

if number > 15:
    print("1")

if first_array:
    print("2")

if len(second_array) == 2:
    print("3")

if len(first_array) + len(second_array) == 5:
    print("4")

if first_array and first_array[0] == 1:
    print("5")

if not second_number:
    print("6")

Expected Output
---------------

test_output_contains("1", no_output_msg= "Did you print out 1 if `number` is greater than 15?")
test_output_contains("2", no_output_msg= "Did you print out 2 if there exists a list `first_array`?")
test_output_contains("3", no_output_msg= "Did you print out 3 if the length of `second_array` is 2?")
test_output_contains("4", no_output_msg= "Did you print out 4 if len(first_array) + len(second_array) == 5?")
test_output_contains("5", no_output_msg= "Did you print out 5 if first_array and first_array[0] == 1?")
test_output_contains("6", no_output_msg= "Did you print out 6 if not second_number?")
success_msg("Great Work!")

Solution
--------

# change this code
number = 16
second_number = 0
first_array = [1,2,3]
second_array = [1,2]

if number > 15:
    print("1")

if first_array:
    print("2")

if len(second_array) == 2:
    print("3")

if len(first_array) + len(second_array) == 5:
    print("4")

if first_array and first_array[0] == 1:
    print("5")

if not second_number:
    print("6")
