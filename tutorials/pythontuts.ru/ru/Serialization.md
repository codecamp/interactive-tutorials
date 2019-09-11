Tutorial
--------

Python предоставляет встроенные библиотеки JSON для кодирования и декодирования JSON.

В Python 2.5 используется модуль simplejson, тогда как в Python 2.7 используется модуль json. Поскольку этот интерпретатор использует Python 2.7, мы будем использовать json.

Чтобы использовать модуль json, он должен сначала быть импортирован:

    import json

Существует два основных формата данных JSON. Либо в строке, либо в объектной структуре данных. Объектная структура данных в Python состоит из списков и словарей, вложенных друг в друга. Объектная структура данных позволяет использовать методы Python (для списков и словарей) для добавления, перечисления, поиска и удаления элементов из структуры данных. Формат String в основном используется для передачи данных в другую программу или загрузки в структуру данных.

Чтобы загрузить JSON обратно в структуру данных, используйте метод «загрузок». Этот метод берет строку и превращает ее обратно в структуру данных объекта json:

    import json 
    print(json.loads(json_string))

Чтобы кодировать структуру данных в JSON, используйте метод «dumps». Этот метод берет объект и возвращает строку:

    import json
    json_string = json.dumps([1, 2, 3, "a", "b", "c"])
    print(json_string)

Python поддерживает собственный метод сериализации данных, называемый pickle (и более быструю альтернативу, называемую cPickle).

Вы можете использовать его точно так же.

    import pickle
    pickled_string = pickle.dumps([1, 2, 3, "a", "b", "c"])
    print(pickle.loads(pickled_string))

Целью упражнения является вывести на экран строку JSON с добавленной к ней парой ключ-значение "Me" : 800.

Tutorial Code
-------------

import json

# fix this function, so it adds the given name
# and salary pair to salaries_json, and return it
def add_employee(salaries_json, name, salary):
    # Add your code here

    return salaries_json

# test code
salaries = '{"Alfred" : 300, "Jane" : 400 }'
new_salaries = add_employee(salaries, "Me", 800)
decoded_salaries = json.loads(new_salaries)
print(decoded_salaries["Alfred"])
print(decoded_salaries["Jane"])
print(decoded_salaries["Me"])

Expected Output
---------------

test_output_contains("300")
test_output_contains("400")
test_output_contains("800")
success_msg("Great work!")

Solution
--------

import json

# fix this function, so it adds the given name
# and salary pair to salaries_json, and return it
def add_employee(salaries_json, name, salary):
    salaries = json.loads(salaries_json)
    salaries[name] = salary

    return json.dumps(salaries)

# test code
salaries = '{"Alfred" : 300, "Jane" : 400 }'
new_salaries = add_employee(salaries, "Me", 800)
decoded_salaries = json.loads(new_salaries)
print(decoded_salaries["Alfred"])
print(decoded_salaries["Jane"])
print(decoded_salaries["Me"])
