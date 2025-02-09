Tutorial
--------

Python является очень простым языком и имеет очень простой синтаксис.
Это вдохновляет программистов программировать без шаблонного (заранее подготовленного) кода.
TСамая простая директива в Python - это директива print -
iона просто печатает строку (и, в отличие от C, включает новую строку).

Существует две основные версии Python: Python 2 и Python 3. Python 2 и 3 совершенно разные.
В этом уроке используется Python 3, поскольку он более семантически корректен и поддерживает новые функции.

Например, одним отличием между Python 2 и 3 является оператор `print`.
В Python 2 оператор print не является функцией, и поэтому он вызывается без скобок. Однако в Python 3 это функция, которая должна вызываться в скобках.

Чтобы напечатать строку в Python 3, просто напишите:

    print("This line will be printed.")

### Отступ

Python использует для блоков отступ вместо фигурных скобок. Поддерживаются как табуляции, так и пробелы, но для стандартного 
отступа требуется, чтобы стандартный код Python использовал четыре пробела. Например:

    x = 1
    if x == 1:
        # indented four spaces
        print("x is 1.")

Упражнение
--------

Используйте команду "print" для печати строки «Hello, World!».

Tutorial Code
-------------

print("Goodbye, World!")

Expected Output
---------------
test_output_contains("Hello, World!")
success_msg('Great job!')

Solution
--------

print("Hello, World!")


