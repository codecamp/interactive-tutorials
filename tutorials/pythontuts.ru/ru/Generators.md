Tutorial
--------

Генераторы очень просты в реализации, но немного сложны для понимания.

Генераторы используются для создания итераторов, но с другим подходом. Генераторы - это простые функции, которые возвращают итеративный набор элементов, по одному, особым образом.

Когда итерация для набора элементов начинает использовать оператор for, запускается генератор. Как только код функции генератора достигает оператора yield, генератор возвращает свое выполнение обратно в цикл for, возвращая новое значение из набора. Функция генератора может генерировать столько значений (возможно, бесконечное множество), сколько она хочет, возвращая каждое из них в свою очередь.

Вот простой пример функции генератора, которая возвращает 7 случайных целых чисел:

      import random
      
      def lottery():
          # returns 6 numbers between 1 and 40
          for i in range(6):
              yield random.randint(1, 40)
      
          # returns a 7th number between 1 and 15
          yield random.randint(1,15)
      
      for random_number in lottery():
             print("And the next number is... %d!" %(random_number))

Эта функция сама решает, как генерировать случайные числа, и выполняет операторы yield поочередно, делая паузу между ними, чтобы вернуть выполнение к основному циклу for.

Упражнение
--------

Напишите функцию генератора, которая возвращает ряд Фибоначчи. Он рассчитывается по следующей формуле: первые два числа серии всегда равны 1, и каждое последовательное возвращенное число является суммой двух последних чисел.
Подсказка: вы можете использовать только две переменные в функции генератора? Помните, что задания могут выполняться одновременно. Код

    a = 1
    b = 2
    a, b = b, a
    print(a,b)

будет одновременно переключать значения a и b.

Tutorial Code
-------------

# fill in this function
def fib():
    pass #this is a null statement which does nothing when executed, useful as a placeholder.

# testing code
import types
if type(fib()) == types.GeneratorType:
    print("Good, The fib function is a generator.")

    counter = 0
    for n in fib():
        print(n)
        counter += 1
        if counter == 10:
            break



Expected Output
---------------

test_output_contains("Good, The fib function is a generator.")
success_msg('Good work!')

Solution
--------

# fill in this function
def fib():
    a, b = 1, 1
    while 1:
        yield a
        a, b = b, a + b

# testing code
import types
if type(fib()) == types.GeneratorType:
    print("Good, The fib function is a generator.")

    counter = 0
    for n in fib():
        print(n)
        counter += 1
        if counter == 10:
            break
