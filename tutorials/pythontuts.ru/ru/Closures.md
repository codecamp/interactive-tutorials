Tutorial
--------

Замыкание - это функциональный объект, который запоминает значения во вложенных областях, даже если они отсутствуют в памяти. Давайте пройдем шаг за шагом

Во-первых, **Вложенная Функция** это функция, определенная внутри другой функции. Очень важно отметить, что вложенные функции могут обращаться к переменным вмещающей области. Тем не менее, по крайней мере в Python, они доступны только для чтения. Однако с этими переменными можно явно использовать ключевое слово «nonlocal», чтобы изменить их.

Например:

    def transmit_to_space(message):
        "This is the enclosing function"
        def data_transmitter():
            "The nested function"
            print(message)
    
        data_transmitter()
    
    print(transmit_to_space("Test message"))

Вариант хорошо работает, так как функция «data_transmitter» может получить доступ к «сообщению». Чтобы продемонстрировать использование нелокального ключевого слова, рассмотрите следующее

    def print_msg(number):
        def printer():
            "Here we are using the nonlocal keyword"
            nonlocal number
            number=3
            print(number)
        printer()
        print(number)
    
    print_msg(9)

Без нелокального ключевого слова результат будет "3 9", однако при его использовании мы получим "3 3", то есть значение переменной "number" будет изменено.

Теперь давайте вернемся к объекту функции, а не к вызову вложенной функции. (Помните, что даже функции являются объектами. (Это Python.))

    def transmit_to_space(message):
        "This is the enclosing function"
        def data_transmitter():
            "The nested function"
            print(message)
        return data_transmitter

И мы вызываем функцию следующим образом:


      def transmit_to_space(message):
        "This is the enclosing function"
        def data_transmitter():
            "The nested function"
            print(message)
        return data_transmitter
        
  	  fun2 = transmit_to_space("Burn the Sun!")
  	  fun2()

Несмотря на то, что выполнение функции "trans_to_space ()" было завершено, сообщение было скорее вчего сохранено. Эта техника, с помощью которой данные прикрепляются к некоторому коду даже после завершения тех других исходных функций, называется в Python замыканиями.

ПРЕИМУЩЕСТВО: Замыкания могут избежать использования глобальных переменных и предоставляют некоторую форму сокрытия данных (например, когда в классе мало методов, используйте вместо этого замыкания).

Кроме того, Декораторы в Python широко используют замыкания.

Упражнение
--------

Сделайте вложенный цикл и замыкание Python, чтобы сделать функции для получения нескольких функций умножения с использованием замыканий. То есть, используя замыкания, можно создавать функции для создания функций multiply_with_5 () или multiply_with_4 () с использованием замыканий.

Tutorial Code
-------------

# your code goes here

multiplywith5 = multiplier_of(5)
multiplywith5(9)

Expected Output
---------------

test_output_contains("45")
success_msg("Great work!")

Solution
--------

def multiplier_of(n):
    def multiplier(number):
        return number*n
    return multiplier

multiplywith5 = multiplier_of(5)
print(multiplywith5(9))
