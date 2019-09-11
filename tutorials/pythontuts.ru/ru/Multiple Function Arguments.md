Tutorial
--------

Каждая функция в Python получает заранее определенное количество аргументов, если они объявлены нормальным образом, например так:

    def myfunction(first, second, third):
        # do something with the 3 variables
        ...

Можно объявить функции, которые получают переменное число аргументов, используя следующий синтаксис:

    def foo(first, second, third, *therest):
        print("First: %s" % first)
        print("Second: %s" % second)
        print("Third: %s" % third)
        print("And all the rest... %s" % list(therest))

Переменная "therest" - это список переменных, который получает все аргументы, которые были переданы функции "foo" после первых 3 аргументов. Поэтому вызов `foo(1,2,3,4,5)` выведет:

    def foo(first, second, third, *therest):
        print("First: %s" %(first))
        print("Second: %s" %(second))
        print("Third: %s" %(third))
        print("And all the rest... %s" %(list(therest)))
    
    foo(1,2,3,4,5)

Также возможно посылать аргументы функций по ключевым словам таким образом, что порядок аргументов не будет иметь значения, используя следующий синтаксис. Следующий код дает такой результат: 
```The sum is: 6
    Result: 1```

    def bar(first, second, third, **options):
        if options.get("action") == "sum":
            print("The sum is: %d" %(first + second + third))
    
        if options.get("number") == "first":
            return first
    
    result = bar(1, 2, 3, action = "sum", number = "first")
    print("Result: %d" %(result))



Функция "bar" получает 3 аргумента. Если получен дополнительный аргумент "action" и он дает инструкции по суммированию чисел, сумма выводится. Кроме того, функция также знает, что она должна вернуть первый аргумент, если значение параметра "number", переданное в функцию, равно "first".

Упражнение
--------

Заполните функции `foo` и` bar`, чтобы они могли получать переменное количество аргументов (3 или более)
Функция `foo` должна возвращать количество полученных дополнительных аргументов.
"Bar" должен возвращать "True", если аргумент с ключевым словом "magicnumber" стоит 7, а в противном случае "False"

Tutorial Code
-------------

# edit the functions prototype and implementation
def foo(a, b, c):
    pass

def bar(a, b, c):
    pass


# test code
if foo(1,2,3,4) == 1:
    print("Good.")
if foo(1,2,3,4,5) == 2:
    print("Better.")
if bar(1,2,3,magicnumber = 6) == False:
    print("Great.")
if bar(1,2,3,magicnumber = 7) == True:
    print("Awesome!")

Expected Output
---------------

test_output_contains("Good.")
test_output_contains("Better.")
test_output_contains("Great.")
test_output_contains("Awesome!")
success_msg("Great work!")

Solution
--------
# edit the functions prototype and implementation
def foo(a, b, c, *args):
    return len(args)

def bar(a, b, c, **kwargs):
    return kwargs["magicnumber"] == 7


# test code
if foo(1,2,3,4) == 1:
    print("Good.")
if foo(1,2,3,4,5) == 2:
    print("Better.")
if bar(1,2,3,magicnumber = 6) == False:
    print("Great.")
if bar(1,2,3,magicnumber = 7) == True:
    print("Awesome!")
