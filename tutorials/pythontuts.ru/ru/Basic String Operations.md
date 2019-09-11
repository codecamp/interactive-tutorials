Tutorial
--------

Строки - это биты текста. Они могут быть определены как что-либо, заключенное в кавычки:

    astring = "Hello world!"
    astring2 = 'Hello world!'

Как видите, первое, чему вы научились, это вывести на экран простое предложение. Это предложение было сохранено Python в виде строки. Однако вместо того, чтобы немедленно выводить строки, мы рассмотрим различные варианты вашего на них воздействия. Вы также можете использовать одинарные кавычки для назначения строки. Однако вы столкнетесь с проблемами, если назначаемое значение само содержит одинарные кавычки. Например, чтобы назначить строку в этих скобках (одинарные кавычки ' '), вам нужно использовать только двойные кавычки, как например

    astring = "Hello world!"
    print("single quotes are ' '")

    print(len(astring))

При этом выводится 12, потому что "Hello world!" – это 12 символов, включая знаки препинания и пробелы.

    astring = "Hello world!"
    print(astring.index("o"))

В таком варианте  выводится 4, потому что местоположение первого вхождения буквы «о» находится на расстоянии 4 символов от первого символа. Обратите внимание на то, что в этой фразе на самом деле два «о» - этот метод распознает только первое.

Но почему он не распечатал 5? Разве «о» не является пятым символом в строке? Чтобы упростить задачу, Python (и большинство других языков программирования) начинают с 0 вместо 1. Таким образом, индекс «o» равен 4.

    astring = "Hello world!"
    print(astring.count("l"))

Для тех из вас, кто использует смешные шрифты, это строчная буква L, а не номер один. Выражение подсчитывает количество l в строке. Поэтому должно быть напечатано 3.

    astring = "Hello world!"
    print(astring[3:7])

Выводится фрагмент строки, начиная с индекса 3 и заканчивая индексом 6. Но почему 6, а не 7? Опять же, большинство языков программирования так делают - это упрощает математику в этих скобках.

Если у вас есть только одно число в скобках, оно даст вам один символ с этим индексом. Если вы пропустите первый номер, но оставите двоеточие, оно даст вам фрагмент от начала до номера, который вы оставили. Если вы пропустите второй номер, он даст вам фрагмент от первого номера до конца.

Вы можете даже поставить отрицательные числа в скобках. Это простой способ начать с конца строки, а не с начала. Таким образом, -3 означает «3-й символ с конца».

    astring = "Hello world!"
    print(astring[3:7:2])

Выводятся символы строки от 3 до 7, пропуская один символ. Это расширенный синтаксис слайса. Общая форма: [старт: стоп: шаг].

    astring = "Hello world!"
    print(astring[3:7])
    print(astring[3:7:1])

Обратите внимание, что оба они дают одинаковый результат

В C нет функции, подобной strrev, для обращения строки. Но с вышеупомянутым типом синтаксиса слайса вы можете легко перевернуть строку, например так

    astring = "Hello world!"
    print(astring[::-1])

Так

    astring = "Hello world!"
    print(astring.upper())
    print(astring.lower())

Они создают новую строку со всеми буквами, преобразованными в верхний и нижний регистр соответственно.

    astring = "Hello world!"
    print(astring.startswith("Hello"))
    print(astring.endswith("asdfasdfasdf"))

Это используется для определения, начинается ли строка с чего-либо или заканчивается чем-то, соответственно. Первый выводит True, так как строка начинается с «Hello». Второй выводит False, так как строка определенно не заканчивается на «asdfasdfasdf».

    astring = "Hello world!"
    afewwords = astring.split(" ")

Разбивает строку на связку строк, сгруппированных в списке. Поскольку этот пример разделяется пробелом, первым элементом в списке будет «Hello», а вторым будет «world!».

Упражнение
--------

Попробуйте исправить код, чтобы вывести правильную информацию, изменив строку.

Tutorial Code
-------------

s = "Hey there! what should this string be?"
# Length should be 20
print("Length of s = %d" % len(s))

# First occurrence of "a" should be at index 8
print("The first occurrence of the letter a = %d" % s.index("a"))

# Number of a's should be 2
print("a occurs %d times" % s.count("a"))

# Slicing the string into bits
print("The first five characters are '%s'" % s[:5]) # Start to 5
print("The next five characters are '%s'" % s[5:10]) # 5 to 10
print("The thirteenth character is '%s'" % s[12]) # Just number 12
print("The characters with odd index are '%s'" %s[1::2]) #(0-based indexing)
print("The last five characters are '%s'" % s[-5:]) # 5th-from-last to end

# Convert everything to uppercase
print("String in uppercase: %s" % s.upper())

# Convert everything to lowercase
print("String in lowercase: %s" % s.lower())

# Check how a string starts
if s.startswith("Str"):
    print("String starts with 'Str'. Good!")

# Check how a string ends
if s.endswith("ome!"):
    print("String ends with 'ome!'. Good!")

# Split the string into three separate strings,
# each containing only a word
print("Split the words of the string: %s" % s.split(" "))

Expected Output
---------------

test_object("s", incorrect_msg="Make sure you change the string assigned to `s` to match the Упражнение instructions.")
success_msg("Great work!")

Solution
--------

s = "Strings are awesome!"
# Length should be 20
print("Length of s = %d" % len(s))

# First occurrence of "a" should be at index 8
print("The first occurrence of the letter a = %d" % s.index("a"))

# Number of a's should be 2
print("a occurs %d times" % s.count("a"))

# Slicing the string into bits
print("The first five characters are '%s'" % s[:5]) # Start to 5
print("The next five characters are '%s'" % s[5:10]) # 5 to 10
print("The thirteenth character is '%s'" % s[12]) # Just number 12
print("The characters with odd index are '%s'" %s[1::2]) #(0-based indexing)
print("The last five characters are '%s'" % s[-5:]) # 5th-from-last to end

# Convert everything to uppercase
print("String in uppercase: %s" % s.upper())

# Convert everything to lowercase
print("String in lowercase: %s" % s.lower())

# Check how a string starts
if s.startswith("Str"):
    print("String starts with 'Str'. Good!")

# Check how a string ends
if s.endswith("ome!"):
    print("String ends with 'ome!'. Good!")

# Split the string into three separate strings,
# each containing only a word
print("Split the words of the string: %s" % s.split(" "))
