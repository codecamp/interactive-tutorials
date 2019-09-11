Tutorial
--------
Получение входных данных и отображение выходных данных необходимым образом играет важную роль в интерактивном кодировании. Итак, давайте сосредоточимся на вводе и выводе различных типов данных.

###raw_input()
используется для получения ввода до тех пор, пока не достигнет конца строки. Обратите внимание, что пробелов быть не должно.  Получение входных данных заканчивается символом новой строки, и если в строке ввода есть пробелы, это приводит к ошибке

    # Prints out the input received from stdin
    astring=raw_input()# give hello as input
    print raw_input()

после ввода мы можем преобразовать их в требуемый тип данных, используя такие функции, как int(),float(),str()

    num=int(raw_input())
    print num
    decimalnum=raw_input()
    decimalnum=float(raw_input()
    print decimalnum

###input()
используется для ввода целых чисел. Преимущество  input() перед raw_input() можно прояснить с помощью следующего примера

    #give 2*2 as input
    a=input()
    b=raw_input() #note that int(raw_input()) results in error
    print a #prints 4
    print b #prints 2*2

###Как принять два или более типа данных в качестве ввода из одной строки, разделенной пробелами?
Здесь мы используем функции  split() и map()

    #give two integers in first line and more than two integers in third line
    a,b=map(int,raw_input().split()
    array=raw_input().split()
    sum=0
    for each in array:
        sum=sum+int(each)
    print a,b,sum #prints first two integers from first line and sum of integers of second line

###Форматирование вывода
Возможно, вы уже заметили, что оператор print автоматически вставляет новую строку. Использование запятой, как в приведенном выше коде, выводит значения в одну строку, разделенные пробелом. Модуль sys предоставляет различные функции для форматирования вывода, но здесь мы узнаем, как использовать базовые знания о форматировании для вывода требуемым способом. Давайте посмотрим несколько примеров, чтобы научиться форматированию вывода

    a=5
    b=0.63
    c="hello"
    print "a is : %d, b is %0.4f,c is %s" %(a,b,c)

Вывод должен быть самоочевидным.
