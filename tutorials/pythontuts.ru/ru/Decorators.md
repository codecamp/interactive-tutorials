Tutorial
--------

Декораторы позволяют вам вносить простые изменения в вызываемые объекты, такие как  [функции](http://www.pythontuts.org/en/Functions ""), [методы, или классы](http://www.pythontuts.org/en/Classes%20and%20Objects ""). Мы разберемся с функциями в этом уроке. Синтаксис

    @decorator
    def functions(arg):
        return "value"

Эквивалентно:

    def function(arg):
        return "value"
    function = decorator(function) # this passes the function to the decorator, and reassigns it to the functions

Как вы, наверное, видели, декоратор - это просто еще одна функция, которая принимает функции и возвращает одну. Например, вы можете сделать следующее:

    def repeater(old_function):
        def new_function(*args, **kwds): # See pythontuts.org/page/Multiple%20Function%20Arguments for how *args and **kwds works
            old_function(*args, **kwds) # we run the old function
            old_function(*args, **kwds) # we do it twice
        return new_function # we have to return the new_function, or it wouldn't reassign it to the value

Это заставит функцию повториться дважды.

    >>> @repeater
    def multiply(num1, num2):
        print(num1 * num2)

    >>> multiply(2, 3)
    6
    6

Вы также можете заставить ее изменить результат

    def double_out(old_function):
        def new_function(*args, **kwds):
            return 2 * old_function(*args, **kwds) # modify the return value
        return new_function

изменить ввод

    def double_Ii(old_function):
        def new_function(arg): # only works if the old function has one argument
            return old_function(arg * 2) # modify the argument passed
        return new_function

и выполнить проверку.

    def check(old_function):
        def new_function(arg):
            if arg < 0: raise (ValueError, "Negative Argument") # This causes an error, which is better than it doing the wrong thing
            old_function(arg)
        return new_function

Допустим, вы хотите умножить результат на переменную сумму. Вы можете определить декоратор и использовать его следующим образом: 

    def multiply(multiplier):
        def multiply_generator(old_function):
            def new_function(*args, **kwds):
                return multiplier * old_function(*args, **kwds)
            return new_function
        return multiply_generator # it returns the new generator
    
    # Usage
    @multiply(3) # multiply is not a generator, but multiply(3) is
    def return_num(num):
        return num
        
    # Now return_num is decorated and reassigned into itself
    return_num(5) # should return 15

 Вы можете делать все что угодно со старой функцией, даже полностью игнорировать ее! Продвинутые декораторы также могут манипулировать строкой документа и номером аргумента.
Для получения информации по некоторым интересным декораторам, перейдите по ссылке  <http://wiki.python.org/moin/PythonDecoratorLibrary>.

Упражнение
--------
Создайте фабрику декораторов, которая возвращает декоратор,  декорирующий функции одним аргументом. Фабрика должна принимать один аргумент, тип, а затем возвращает декоратор, который заставляет функцию проверять, является ли тип ввода правильным. Если это не так, он должен напечатать («Плохой тип») (На самом деле, это должно вызвать ошибку, но сообщение об ошибке обсуждается не в этом уроке). Посмотрите учебный код и ожидаемый результат, чтобы понять, что это такое, если вы запутались (я бы точно запутался). Использование isinstance (object, type_of_object) или type (object) может помочь.

Tutorial Code
-------------
def type_check(correct_type):
    #put code here

@type_check(int)
def times2(num):
    return num*2

print(times2(2))
times2('Not A Number')

@type_check(str)
def first_letter(word):
    return word[0]

print(first_letter('Hello World'))
first_letter(['Not', 'A', 'String'])


Expected Output
---------------

test_output_contains("4")
test_output_contains("Bad Type")
test_output_contains("H")
test_output_contains("Bad Type")
success_msg("Good job!")

Solution
--------

def type_check(correct_type):
    def check(old_function):
        def new_function(arg):
            if (isinstance(arg, correct_type)):
                return old_function(arg)
            else:
                print("Bad Type")
        return new_function
    return check

@type_check(int)
def times2(num):
    return num*2

print(times2(2))
times2('Not A Number')

@type_check(str)
def first_letter(word):
    return word[0]

print(first_letter('Hello World'))
first_letter(['Not', 'A', 'String'])
