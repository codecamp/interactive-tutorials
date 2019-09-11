Tutorial
--------

В Python есть два типа циклов: for и while.

### Цикл "for"

Циклы "for" итерируют по заданной последовательности:

    primes = [2, 3, 5, 7]
    for prime in primes:
        print(prime)

Циклы "for" могут выполнять итерацию по последовательности чисел с помощью функций range и xrange. Разница между range и xrange заключается в том, что функция range возвращает новый список с номерами указанного диапазона, тогда как xrange возвращает итератор, что более эффективно. (Python 3 использует функцию range, которая действует как xrange). Обратите внимание, что функция диапазона основана на нуле.

    # Prints out the numbers 0,1,2,3,4
    for x in range(5):
        print(x)

    # Prints out 3,4,5
    for x in range(3, 6):
        print(x)

    # Prints out 3,5,7
    for x in range(3, 8, 2):
        print(x)

### Циклы "while"

Циклы While повторяются, пока выполняется определенное логическое условие. Например:

    # Prints out 0,1,2,3,4

    count = 0
    while count < 5:
        print(count)
        count += 1  # This is the same as count = count + 1

### Операторы "break" и "continue"

**break** используется для выхода из цикла for или цикла while, тогда как **continue** используется для пропуска текущего блока и возврата к выражению "for" или "while". Несколько примеров:

    # Prints out 0,1,2,3,4

    count = 0
    while True:
        print(count)
        count += 1
        if count >= 5:
            break

    # Prints out only odd numbers - 1,3,5,7,9
    for x in range(10):
        # Check if x is even
        if x % 2 == 0:
            continue
        print(x)

### cможем ли мы использовать условие "else" для циклов?

в отличие от таких языков как C, CPP .. мы можем использовать **else** для циклов. Когда условие цикла оператора for или while не выполняется, выполняется часть кода в else. Если оператор цикла **break** выполняется внутри цикла for, тогда часть else будет пропущена.
Обратите внимание, что часть else выполняется, даже если есть оператор **continue**.

Вот несколько примеров:

    # Prints out 0,1,2,3,4 and then it prints "count value reached 5"

    count=0
    while(count<5):
        print(count)
        count +=1
    else:
        print("count value reached %d" %(count))

    # Prints out 1,2,3,4
    for i in range(1, 10):
        if(i%5==0):
            break
        print(i)
    else:
        print("this is not printed because for loop is terminated because of break but not due to fail in condition")


Упражнение
--------

Просмотрите и распечатайте все четные числа из списка номеров в том же порядке, в котором они были получены. Не печатайте цифры, которые появятся в последовательности после 237.

Tutorial Code
-------------
numbers = [
    951, 402, 984, 651, 360, 69, 408, 319, 601, 485, 980, 507, 725, 547, 544,
    615, 83, 165, 141, 501, 263, 617, 865, 575, 219, 390, 984, 592, 236, 105, 942, 941,
    386, 462, 47, 418, 907, 344, 236, 375, 823, 566, 597, 978, 328, 615, 953, 345,
    399, 162, 758, 219, 918, 237, 412, 566, 826, 248, 866, 950, 626, 949, 687, 217,
    815, 67, 104, 58, 512, 24, 892, 894, 767, 553, 81, 379, 843, 831, 445, 742, 717,
    958, 609, 842, 451, 688, 753, 854, 685, 93, 857, 440, 380, 126, 721, 328, 753, 470,
    743, 527
]

# your code goes here

Expected Output
---------------

test_object("number", undefined_msg="Define a object `number` using the code from the tutorial to print just the desired numbers from the Упражнение description.",incorrect_msg="Your `number` object is not correct, You should use an `if` statement and a `break` statement to accomplish your goal.")
success_msg("Great work!")

Solution
--------

numbers = [
    951, 402, 984, 651, 360, 69, 408, 319, 601, 485, 980, 507, 725, 547, 544,
    615, 83, 165, 141, 501, 263, 617, 865, 575, 219, 390, 984, 592, 236, 105, 942, 941,
    386, 462, 47, 418, 907, 344, 236, 375, 823, 566, 597, 978, 328, 615, 953, 345,
    399, 162, 758, 219, 918, 237, 412, 566, 826, 248, 866, 950, 626, 949, 687, 217,
    815, 67, 104, 58, 512, 24, 892, 894, 767, 553, 81, 379, 843, 831, 445, 742, 717,
    958, 609, 842, 451, 688, 753, 854, 685, 93, 857, 440, 380, 126, 721, 328, 753, 470,
    743, 527
]

# your code goes here
for number in numbers:
    if number == 237:
        break

    if number % 2 == 1:
        continue

    print(number)
