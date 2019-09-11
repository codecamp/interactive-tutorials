Tutorial
--------

Списки очень похожи на массивы. Они могут содержать переменные любого типа и могут содержать столько переменных, сколько вы пожелаете. Списки также могут быть перебраны очень простым способом. Вот пример того, как построить список.

    mylist = []
    mylist.append(1)
    mylist.append(2)
    mylist.append(3)
    print(mylist[0]) # prints 1
    print(mylist[1]) # prints 2
    print(mylist[2]) # prints 3

    # prints out 1,2,3
    for x in mylist:
        print(x)

Доступ к несуществующему индексу генерирует исключение (ошибку).

    mylist = [1,2,3]
    print(mylist[10])

Упражнение
--------

В этом упражнении вам нужно будет добавить числа и строки в правильные списки, используя метод списка "append". Вы должны добавить числа 1, 2 и 3 в список "numbers", а слова "hello" и "world" - в строковую переменную.

Вам также нужно будет заполнить переменную second_name вторым именем в списке имен, используя оператор скобок `[]`. Обратите внимание, что индекс начинается с нуля, поэтому, если вы хотите получить доступ ко второму элементу в списке, его индекс будет равен 1.

Tutorial Code
-------------
numbers = []
strings = []
names = ["John", "Eric", "Jessica"]

# write your code here
second_name = None


# this code should write out the filled arrays and the second name in the names list (Eric).
print(numbers)
print(strings)
print("The second name on the names list is %s" % second_name)

Expected Output
---------------

test_output_contains("[1,2,3]", no_output_msg= "Make sure that you have printed the `numbers` list.")
test_output_contains("['hello', 'world']", no_output_msg= "Make sure that you have printed the `strings` list.")
test_output_contains("The second name on the names list is Eric", no_output_msg= "Did you fill in the variable `second_name` with the second name in the names list?")
success_msg("Great Job!")

Solution
--------

numbers = []
strings = []
names = ["John", "Eric", "Jessica"]

# write your code here
numbers.append(1)
numbers.append(2)
numbers.append(3)

strings.append("hello")
strings.append("world")

second_name = names[1]

# this code should write out the filled arrays and the second name in the names list (Eric).
print(numbers)
print(strings)
print("The second name on the names list is %s" % second_name)
