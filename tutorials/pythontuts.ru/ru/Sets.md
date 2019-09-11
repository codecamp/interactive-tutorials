Tutorial
--------

Множества - это списки без повторяющихся записей. Допустим, вы хотите собрать список слов, используемых в абзаце:

    print(set("my name is Eric and Eric is my name".split()))

Распечатается список, содержащий «my», «name», «is», «Eric» и, наконец, «and». Поскольку в остальной части предложения используются слова, которые уже есть в множестве, они не вставляются дважды.

Множества являются мощным инструментом в Python, так как они имеют возможность вычислять различия и пересечения между другими множествами. Например, скажем, у вас есть список участников событий A и B:

    a = set(["Jake", "John", "Eric"])
    print(a)
    b = set(["John", "Jill"])
    print(b)

Чтобы узнать, какие участники посетили оба мероприятия, вы можете использовать метод "пересечения":

    a = set(["Jake", "John", "Eric"])
    b = set(["John", "Jill"])
    
    print(a.intersection(b))
    print(b.intersection(a))

Чтобы выяснить, какие участники посетили только одно из событий, используйте метод "mmetric_difference":

    a = set(["Jake", "John", "Eric"])
    b = set(["John", "Jill"])
    
    print(a.symmetric_difference(b))
    print(b.symmetric_difference(a))

Чтобы выяснить, какие участники посетили только одно мероприятие, а не другое, используйте метод "difference":

    a = set(["Jake", "John", "Eric"])
    b = set(["John", "Jill"])
    
    print(a.difference(b))
    print(b.difference(a))

Чтобы получить список всех участников, используйте метод "union":

    a = set(["Jake", "John", "Eric"])
    b = set(["John", "Jill"])
    
    print(a.union(b))

В приведенном ниже упражнении используйте указанные списки, чтобы распечатать набор, содержащий всех участников события А, которые не посещали событие В.

Tutorial Code
-------------
a = ["Jake", "John", "Eric"]
b = ["John", "Jill"]

Expected Output
---------------
test_output_contains("['Jake', 'Eric']")
success_msg("Nice work!")

Solution
--------
a = ["Jake", "John", "Eric"]
b = ["John", "Jill"]

A = set(a)
B = set(b)

print(A.difference(B))
