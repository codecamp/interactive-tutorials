Tutorial
--------

Python является полностью объектно-ориентированным, а не "статически типизированным". Вам не нужно объявлять переменные перед их использованием или объявлять их тип. Каждая переменная в Python является объектом.

В этом уроке будут рассмотрены несколько основных типов переменных.

### Числа
Python поддерживает два типа чисел - целые числа и числа с плавающей точкой. (Он также поддерживает комплексные числа, которые не будут объясняться в этом уроке).

Чтобы определить целое число, используйте следующий синтаксис:

    myint = 7
    print(myint)

Чтобы определить число с плавающей запятой, вы можете использовать одно из следующих обозначений:

    myfloat = 7.0
    print(myfloat)
    myfloat = float(7)
    print(myfloat)

### Строки

Строки определяются либо одинарными, либо двойными кавычками.

    mystring = 'hello'
    print(mystring)
    mystring = "hello"
    print(mystring)

Разница между ними заключается в том, что использование двойных кавычек позволяет легко включать апострофы (тогда как при использовании одинарных кавычек они завершают строку)

    mystring = "Don't worry about apostrophes"
    print(mystring)
    
Существуют дополнительные варианты определения строк, которые облегчают включение таких вещей, как возврат каретки, обратная косая черта и символы Unicode. Они выходят за рамки этого руководства, но описаны в  [документации по Python](http://docs.python.org/tutorial/introduction.html#strings "Strings in Python Tutorial").

Простые операторы могут быть выполнены для чисел и строк:

    one = 1
    two = 2
    three = one + two
    print(three)

    hello = "hello"
    world = "world"
    helloworld = hello + " " + world
    print(helloworld)

Назначения могут быть сделаны для более чем одной переменной "одновременно" в одной строке следующим образом

    a, b = 3, 4
    print(a,b)

Смешивание операторов между числами и строками не поддерживается:

    # This will not work!
    one = 1
    two = 2
    hello = "hello"
    
    print(one + two + hello)


Упражнение
--------

Цель этого упражнения - создать строку, целое число и число с плавающей запятой. Строка должна называться mystring и содержать слово «hello». Число с плавающей запятой должно называться myfloat и должно содержать число 10.0, а целое число должно называться myint и должно содержать число 20.

Tutorial Code
-------------
# change this code
mystring = None
myfloat = None
myint = None

# testing code
if mystring == "hello":
    print("String: %s" % mystring)
if isinstance(myfloat, float) and myfloat == 10.0:
    print("Float: %f" % myfloat)
if isinstance(myint, int) and myint == 20:
    print("Integer: %d" % myint)

Expected Output
---------------

test_object('mystring', incorrect_msg="Don't forget to change `mystring` to the correct value from the Упражнение description.")
test_object('myfloat', incorrect_msg="Don't forget to change `myfloat` to the correct value from the Упражнение description.")
test_object('myint', incorrect_msg="Don't forget to change `myint` to the correct value from the Упражнение description.")
test_output_contains("String: hello",no_output_msg= "Make sure your string matches exactly to the Упражнение desciption.")
test_output_contains("Float: 10.000000",no_output_msg= "Make sure your float matches exactly to the Упражнение desciption.")
test_output_contains("Integer: 20",no_output_msg= "Make sure your integer matches exactly to the Упражнение desciption.")
success_msg("Great job!")

Solution
--------

# change this code
mystring = "hello"
myfloat = 10.0
myint = 20

# testing code
if mystring == "hello":
    print("String: %s" % mystring)
if isinstance(myfloat, float) and myfloat == 10.0:
    print("Float: %f" % myfloat)
if isinstance(myint, int) and myint == 20:
    print("Integer: %d" % myint)
