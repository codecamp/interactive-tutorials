Tutorial
-----------------

Объекты - это инкапсуляция переменных и функций в единый объект. Объекты получают свои переменные и функции от классов. Классы по сути являются шаблоном для создания ваших объектов.

Очень простой класс будет выглядеть примерно так:

    class MyClass:
        variable = "blah"

        def function(self):
            print("This is a message inside the class.")

Мы объясним, почему вы должны включить это «self» в качестве параметра чуть позже. Во-первых, чтобы присвоить объекту вышеупомянутый класс (шаблон), вы должны сделать следующее:

    class MyClass:
        variable = "blah"

        def function(self):
            print("This is a message inside the class.")

    myobjectx = MyClass()

Теперь переменная «myobjectx» содержит объект класса «MyClass», который содержит переменную и функцию, определенную в классе «MyClass».

### Доступ к объектным переменным

Чтобы получить доступ к переменной внутри вновь созданного объекта "myobjectx", вы должны сделать следующее:

    class MyClass:
        variable = "blah"

        def function(self):
            print("This is a message inside the class.")

    myobjectx = MyClass()

    myobjectx.variable

Так, например, ниже будет выводиться строка "blah":

    class MyClass:
        variable = "blah"

        def function(self):
            print("This is a message inside the class.")

    myobjectx = MyClass()

    print(myobjectx.variable)

Вы можете создать несколько разных объектов одного и того же класса (с одинаковыми переменными и определенными функциями). Однако каждый объект содержит независимые копии переменных, определенных в классе. Например, если нам нужно определить другой объект с классом «MyClass», а затем изменить строку в переменной выше:

    class MyClass:
        variable = "blah"

        def function(self):
            print("This is a message inside the class.")

    myobjectx = MyClass()
    myobjecty = MyClass()

    myobjecty.variable = "yackity"

    # Then print out both values
    print(myobjectx.variable)
    print(myobjecty.variable)


### Доступ к функциям объекта

Для доступа к функции внутри объекта вы используете нотацию, аналогичную доступу к переменной:

    class MyClass:
        variable = "blah"

        def function(self):
            print("This is a message inside the class.")

    myobjectx = MyClass()

    myobjectx.function()

Выражение выше будет выводить сообщение «Это сообщение внутри класса»


Упражнение
--------

У нас есть класс, определенный для транспортных средств. Создайте два новых автомобиля с именами car1 и car2. Сделайте car1 красным кабриолетом стоимостью 60 000 долларов США с именем Fer, а car2 - синий фургон с именем Jump стоимостью 10 000 долларов США.

Tutorial Code
-------------

# define the Vehicle class
class Vehicle:
    name = ""
    kind = "car"
    color = ""
    value = 100.00
    def description(self):
        desc_str = "%s is a %s %s worth $%.2f." % (self.name, self.color, self.kind, self.value)
        return desc_str
# your code goes here

# test code
print(car1.description())
print(car2.description())

Expected Output
---------------

#test_output_contains('Fer is a red convertible worth $60000.00.')
#test_output_contains('Jump is a blue van worth $10000.00.')
success_msg("Great job!")

Solution
--------

# define the Vehicle class
class Vehicle:
    name = ""
    kind = "car"
    color = ""
    value = 100.00
    def description(self):
        desc_str = "%s is a %s %s worth $%.2f." % (self.name, self.color, self.kind, self.value)
        return desc_str

# your code goes here
car1 = Vehicle()
car1.name = "Fer"
car1.color = "red"
car1.kind = "convertible"
car1.value = 60000.00

car2 = Vehicle()
car2.name = "Jump"
car2.color = "blue"
car2.kind = "van"
car2.value = 10000.00

# test code
print(car1.description())
print(car2.description())
