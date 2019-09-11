Tutorial
--------

Вы можете создавать частично определенные функции в Python, используя частично определенную функцию из библиотеки functools.

Частично определенные функции позволяют получить функцию с x параметрами для функции с меньшим количеством параметров и фиксированных значений, установленных для более ограниченной функции.

Требуемый импорт:

    from functools import partial

Этот код вернет 8.

    from functools import partial
    
    def multiply(x,y):
            return x * y
    
    # create a new function that multiplies by 2
    dbl = partial(multiply,2)
    print(dbl(4))

Важное примечание: значения по умолчанию начнут заменять переменные слева. 2 заменит х. y будет равно 4, когда будет вызываться dbl (4). Для этого примера разницы нет, но она есть в примере ниже.

Упражнение
--------
Отредактируйте предоставленную функцию, вызвав метод part () и заменив первые три переменные в функции func (). Затем выведите на экран с новой частично определенной функцией, используя только одну входную переменную, чтобы результат был равен 60.


Tutorial Code
-------------
#Following is the Упражнение, function provided:
from functools import partial
def func(u,v,w,x):
    return u*4 + v*3 + w*2 + x
#Enter your code here to create and print with your partial function

Expected Output
---------------
#test_object('p')
test_output_contains('60')
success_msg('Good job!')

Solution
--------
from functools import partial
def func(u,v,w,x):
    return u*4 + v*3 + w*2 + x

p = partial(func,5,6,7)
print(p(8))
