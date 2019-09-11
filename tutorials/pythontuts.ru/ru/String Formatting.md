Tutorial
--------

Python использует форматирование строк в стиле C для создания новых форматированных строк. Оператор «%» используется для форматирования набора переменных, заключенных в «кортеж» (список фиксированного размера), вместе со строкой форматирования, которая содержит обычный текст вместе с «спецификаторами аргумента», специальными символами, такими как «% s» и "% d".

Допустим, у вас есть переменная с именем «name» с вашим именем пользователя, и вы хотели бы затем вывести (приветствие этому пользователю).

    # This prints out "Hello, John!"
    name = "John"
    print("Hello, %s!" % name)

Чтобы использовать два или более спецификатора аргумента, используйте кортеж (круглые скобки):

    # This prints out "John is 23 years old."
    name = "John"
    age = 23
    print("%s is %d years old." % (name, age))

Любой объект, который не является строкой, также может быть отформатирован с использованием оператора % s. Строка, которая возвращается из метода «repr» этого объекта, форматируется как строка. Например:

    # This prints out: A list: [1, 2, 3]
    mylist = [1,2,3]
    print("A list: %s" % mylist)

Вот некоторые основные спецификаторы аргументов, которые вы должны знать:


`%s - String (or any object with a string representation, like numbers)`

`%d - Integers`

`%f - Floating point numbers`

`%.<number of digits>f - Floating point numbers with a fixed amount of digits to the right of the dot.`

`%x/%X - Integers in hex representation (lowercase/uppercase)`


Упражнение
--------

Вам нужно будет написать строку формата, которая выводит данные, используя следующий синтаксис:
    `Hello John Doe. Your current balance is $53.44.`

Tutorial Code
-------------

data = ("John", "Doe", 53.44)
format_string = "Hello"

print(format_string % data)

Expected Output
---------------
#test_output_contains("Hello John Doe. Your current balance is $53.44.", no_output_msg= "Make sure you add the `%s` in the correct spaces to the `format_string` to meeet the Упражнение goals!")
test_object('format_string')
success_msg('Great work!')

Solution
--------

data = ("John", "Doe", 53.44)
format_string = "Hello %s %s. Your current balance is $%s."

print(format_string % data)
