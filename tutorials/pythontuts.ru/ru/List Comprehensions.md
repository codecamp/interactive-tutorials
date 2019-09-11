Tutorial
--------

Генераторы списков - очень мощный инструмент, который создает новый список на основе другого списка в единственной читаемой строке.

Например, скажем, нам нужно создать список целых чисел, которые определяют длину каждого слова в определенном предложении, но только если слово не является словом "the".

    sentence = "the quick brown fox jumps over the lazy dog"
    words = sentence.split()
    word_lengths = []
    for word in words:
          if word != "the":
              word_lengths.append(len(word))
    print(words)
    print(word_lengths)

Используя генератор списка, мы могли бы упростить этот процесс до следующих обозначений:

    sentence = "the quick brown fox jumps over the lazy dog"
    words = sentence.split()
    word_lengths = [len(word) for word in words if word != "the"]
    print(words)
    print(word_lengths)

Упражнение
--------

Используя генератор списка, создайте новый список с именем "newlist" из списка "numbers", который содержит только положительные числа из списка в виде целых чисел.

Tutorial Code
-------------
numbers = [34.6, -203.4, 44.9, 68.3, -12.2, 44.6, 12.7]
newlist = []
print(newlist)

Expected Output
---------------

test_output_contains("[34, 44, 68, 44, 12]")
success_msg("Very nice!")

Solution
--------
numbers = [34.6, -203.4, 44.9, 68.3, -12.2, 44.6, 12.7]
newlist = [int(x) for x in numbers if x > 0]
print(newlist)
