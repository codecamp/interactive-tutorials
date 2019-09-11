Tutorial
--------

Интроспекция кода - это способность исследовать классы, функции и ключевые слова, чтобы узнать, что они из себя представляют, что они делают и что они знают.

Python предоставляет несколько функций и утилит для интроспекции кода.

    help()
    dir() 
    hasattr() 
    id() 
    type() 
    repr() 
    callable() 
    issubclass() 
    isinstance() 
    __doc__ 
    __name__ 
    

Часто наиболее важной является функция справки, так как вы можете использовать ее, чтобы узнать, что делают другие функции.

Упражнение
--------

Вывести на экран список всех атрибутов данного объекта Vehicle.

Tutorial Code
-------------

# Use the help function to see what each function does.
# Delete this when you are done.
help(dir)
help(hasattr)
help(id)

# Define the Vehicle class.
class Vehicle:
    name = ""
    kind = "car"
    color = ""
    value = 100.00
    def description(self):
        desc_str = "%s is a %s %s worth $%.2f." % (self.name, self.color, self.kind, self.value)
        return desc_str

# Print a list of all attributes of the Vehicle class.
# Your code goes here


Expected Output
---------------

test_output_contains("['__doc__', '__module__', 'color', 'description', 'kind', 'name', 'value']")
test_student_typed("print")
success_msg("Very nice!")

Solution
--------

# Define the Vehicle class
class Vehicle:
    name = ""
    kind = "car"
    color = ""
    value = 100.00
    def description(self):
        desc_str = "%s is a %s %s worth $%.2f." % (self.name, self.color, self.kind, self.value)
        return desc_str

# Print a list of all attributes of the Vehicle class.
print(dir(Vehicle))
