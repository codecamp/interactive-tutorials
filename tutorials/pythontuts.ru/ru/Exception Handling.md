Tutorial
--------
При программировании случаются ошибки. Это просто факт жизни.
Возможно, пользователь дал неверные данные. Возможно, сетевой ресурс был недоступен. 
Возможно, программе не хватило памяти. Или программист, возможно, даже ошибся!

Решением ошибок Python являются исключения. Возможно, вы видели исключение раньше.

    print(a)
    
    #error
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    NameError: name 'a' is not defined

Упс! Забыл присвоить значение переменной 'a'.

Но иногда вы не хотите, чтобы исключения полностью останавливали
программу. Возможно, вы захотите сделать что-то особенное, когда 
возникнет исключение. Это делается в блоке *try/except*.

Вот тривиальный пример: предположим, вы перебираете список. Вам нужно перебрать более 20 номеров, но список составлен из пользовательского ввода и может не содержать 20 номеров. После того, как вы дойдете до конца списка, вы просто хотите, чтобы остальные числа интерпретировались как 0. Вот как вы можете это сделать:

    def do_stuff_with_number(n):
        print(n)
    
    def catch_this():
        the_list = (1, 2, 3, 4, 5)
    
        for i in range(20):
            try:
                do_stuff_with_number(the_list[i])
            except IndexError: # Raised when accessing a non-existing index of a list
                do_stuff_with_number(0)
    
    catch_this()

Вот, не так-то и сложно! Вы можете сделать это с любым исключением. Для получения более подробной информации об обработке исключений, загляните в 
[Python Docs](http://docs.python.org/tutorial/errors.html#handling-exceptions)

Упражнение
--------

Обрабатывать все исключения! Вспомните предыдущие уроки, чтобы вернуть фамилию актера.

Tutorial Code
-------------

# Setup
actor = {"name": "John Cleese", "rank": "awesome"}

# Function to modify!!!
def get_last_name(): 
    return actor["last_name"]

# Test code
get_last_name()
print("All exceptions caught! Good job!")
print("The actor's last name is %s" % get_last_name())

Expected Output
---------------

test_output_contains("Cleese")
test_output_contains("All exceptions caught! Good job!")
test_output_contains("The actor's last name is Cleese")
success_msg("Great work!")

Solution
--------
actor = {"name": "John Cleese", "rank": "awesome"}

def get_last_name():
    return actor["name"].split()[1]

get_last_name()
print("All exceptions caught! Good job!")
print("The actor's last name is %s" % get_last_name())
