Tutorial
--------

### Что такое функции?

Функции - это удобный способ разделить ваш код на полезные блоки, позволяя нам упорядочить наш код, сделать его более читабельным, повторно использовать его и сэкономить некоторое время. Также функции являются ключевым способом определения интерфейсов, чтобы программисты могли делиться своим кодом.

### Как вы пишете функции в Python?

Как мы видели в предыдущих уроках, Python использует блоки.

Блок - это область кода, записанная в формате:

    block_head:
        1st block line
        2nd block line
        ...

Где строка блока - это больше код Python (даже другого блока), а заголовок блока имеет следующий формат:
block_keyword block_name(argument1,argument2, ...)
Ключевыми словами блока, которые вы уже знаете, являются "if", "for", и "while".

Функции в Python определяются с помощью ключевого слова "def", за которым следует имя функции в качестве имени блока. Например:

    def my_function():
        print("Hello From My Function!")


Функции также могут получать аргументы (переменные, передаваемые вызывающим в функцию). Например:

    def my_function_with_args(username, greeting):
        print("Hello, %s , From My Function!, I wish you %s"%(username, greeting))


Функции могут возвращать значение вызывающей стороне, используя ключевое слово 'return'.
Например:

    def sum_two_numbers(a, b):
        return a + b

### Как вы вызываете функции в Python?

Просто напишите имя функции, а затем (), поместив все необходимые аргументы в скобки.
Например, давайте вызовем функции, написанные выше (в предыдущем примере):

    # Define our 3 functions
    def my_function():
        print("Hello From My Function!")

    def my_function_with_args(username, greeting):
        print("Hello, %s , From My Function!, I wish you %s"%(username, greeting))

    def sum_two_numbers(a, b):
        return a + b

    # print(a simple greeting)
    my_function()

    #prints - "Hello, John Doe, From My Function!, I wish you a great year!"
    my_function_with_args("John Doe", "a great year!")

    # after this line x will hold the value 3!
    x = sum_two_numbers(1,2)  


Упражнение
--------

В этом упражнении вы будете использовать существующую функцию и одновременно добавлять свою собственную для создания полнофункциональной программы.

1. Добавьте функцию с именем list_benefits (), которая возвращает следующий список строк: «Более организованный код», «Более читаемый код», «Более простое повторное использование кода», «Предоставление программистам возможности совместно использовать и соединять код вместе»

2. Добавьте функцию с именем build_sentence (info), которая получает единственный аргумент, содержащий строку, и возвращает предложение, начинающееся с данной строки и заканчивающееся строкой «это преимущество функций!»

3. Запустите и убедитесь, что все функции работают вместе!

Tutorial Code
-------------

# Modify this function to return a list of strings as defined above
def list_benefits():
    pass

# Modify this function to concatenate to each benefit - " is a benefit of functions!"
def build_sentence(benefit):
    pass

def name_the_benefits_of_functions():
    list_of_benefits = list_benefits()
    for benefit in list_of_benefits:
        print(build_sentence(benefit))

name_the_benefits_of_functions()


Expected Output
---------------

test_output_contains("More organized code is a benefit of functions!")
test_output_contains("More readable code is a benefit of functions!")
test_output_contains("Easier code reuse is a benefit of functions!")
test_output_contains("Allowing programmers to share and connect code together is a benefit of functions!")
success_msg("Nice work!")

Solution
--------

# Modify this function to return a list of strings as defined above
def list_benefits():
    return "More organized code", "More readable code", "Easier code reuse", "Allowing programmers to share and connect code together"

# Modify this function to concatenate to each benefit - " is a benefit of functions!"
def build_sentence(benefit):
    return "%s is a benefit of functions!" % benefit


def name_the_benefits_of_functions():
    list_of_benefits = list_benefits()
    for benefit in list_of_benefits:
        print(build_sentence(benefit))

name_the_benefits_of_functions()
