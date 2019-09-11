Tutorial
--------

Словарь - это тип данных, аналогичный массивам, но работающий с ключами и значениями вместо индексов. К каждому значению, хранящемуся в словаре, можно получить доступ с помощью ключа, который представляет собой объект любого типа (строку, число, список и т. д.), вместо использования его индекса для его адресации.

Например, база данных телефонных номеров может храниться с использованием словаря, подобного следующему:

    phonebook = {}
    phonebook["John"] = 938477566
    phonebook["Jack"] = 938377264
    phonebook["Jill"] = 947662781
    print(phonebook)

Кроме того, словарь может быть инициализирован с теми же значениями в следующих обозначениях:

    phonebook = {
        "John" : 938477566,
        "Jack" : 938377264,
        "Jill" : 947662781
    }
    print(phonebook)

### Перебор словарей

Словари можно перебирать, как список. Однако словарь, в отличие от списка, не сохраняет порядок значений, хранящихся в нем. Чтобы перебрать пары ключ-значение, используйте следующий синтаксис:
    
    phonebook = {"John" : 938477566,"Jack" : 938377264,"Jill" : 947662781}
    for name, number in phonebook.items():
        print("Phone number of %s is %d" % (name, number))

### Удаление значения

Чтобы удалить указанный индекс, используйте одно из следующих обозначений:
    
    phonebook = {
       "John" : 938477566,
       "Jack" : 938377264,
       "Jill" : 947662781
    }
    del phonebook["John"]
    print(phonebook)

или:
    
    phonebook = {
       "John" : 938477566,
       "Jack" : 938377264,
       "Jill" : 947662781
    }
    phonebook.pop("John")
    print(phonebook)

Упражнение
--------

Добавьте "Jake" в телефонную книгу с номером телефона 938273443 и удалите Jill из телефонной книги.

Tutorial Code
-------------

phonebook = {
    "John" : 938477566,
    "Jack" : 938377264,
    "Jill" : 947662781
}

# write your code here


# testing code
if "Jake" in phonebook:
    print("Jake is listed in the phonebook.")
if "Jill" not in phonebook:
    print("Jill is not listed in the phonebook.")

Expected Output
---------------

test_output_contains("Jake is listed in the phonebook.")
test_output_contains("Jill is not listed in the phonebook.")
success_msg("Nice work!")

Solution
--------

phonebook = {
    "John" : 938477566,
    "Jack" : 938377264,
    "Jill" : 947662781
}

# write your code here
phonebook["Jake"] = 938273443
del phonebook["Jill"]

# testing code
if "Jake" in phonebook:
    print("Jake is listed in the phonebook.")
if "Jill" not in phonebook:
    print("Jill is not listed in the phonebook.")
