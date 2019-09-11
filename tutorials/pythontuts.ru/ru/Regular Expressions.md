Tutorial
--------

Регулярные выражения (иногда сокращенные до regexp, regex или re) являются инструментом для сопоставления шаблонов в тексте. В Python у нас есть модуль re. Применения для регулярных выражений широко распространены, но они довольно сложны, поэтому при рассмотрении использования регулярного выражения для определенной задачи подумайте об альтернативах и прибегайте к регулярным выражениям в качестве средства последней надежды.

Примером регулярного выражения является `r"^(From|To|Cc).*?python-list@python.org"` Проясним: 
символ вставки `^` соответствует тексту в начале строки. Следующая группа, часть с `(From|To|Cc)` означает, что строка должна начинаться с одного из слов, разделенных чертой `|`. Это называется оператором ИЛИ, и регулярное выражение будет совпадать, если строка начинается с любого из слов в группе. `.*?` означает нежадное сопоставление любого количества символов, не считая символа новой строки `\n`. Нежадная часть означает совпадение как можно меньшего числа повторений. Символ `.` означает любой символ с не новой строки, символe `*` означает повторение 0 или более раз, а символ `?` делает его нежадным.

Таким образом, этому регулярному выражению будут соответствовать следующие строки:
`From: python-list@python.org`
`To: !asp]<,.      python-list@python.org`

Полная ссылка на синтаксис re доступна в [python
docs](http://docs.python.org/library/re.html#regular-expression-syntax
"RE синтаксис).

В качестве примера "правильного" регулярного выражения соответствия электронной почты (как в упражнении), смотрите [это](http://www.ex-parrot.com/pdw/Mail-RFC822-Address.html)

Tutorial Code
-------------
# Example: 
import re
pattern = re.compile(r"\[(on|off)\]") # Slight optimization
print(re.search(pattern, "Mono: Playback 65 [75%] [-16.50dB] [on]"))
# Returns a Match object!
print(re.search(pattern, "Nada...:-("))
# Doesn't return anything.
# End Example

# Упражнение: make a regular expression that will match an email
def test_email(your_pattern):
    pattern = re.compile(your_pattern)
    emails = ["john@example.com", "python-list@python.org", "wha.t.`1an?ug{}ly@email.com"]
    for email in emails:
        if not re.match(pattern, email):
            print("You failed to match %s" % (email))
        elif not your_pattern:
            print("Forgot to enter a pattern!")
        else:
            print("Pass")
pattern = r"" # Your pattern here!
test_email(pattern)
    

Expected Output
---------------
test_output_contains("Pass")
success_msg("Great work!")

Solution
--------
# Упражнение: make a regular expression that will match an email
import re
def test_email(your_pattern):
    pattern = re.compile(your_pattern)
    emails = ["john@example.com", "python-list@python.org", "wha.t.`1an?ug{}ly@email.com"]
    for email in emails:
        if not re.match(pattern, email):
            print("You failed to match %s" % (email))
        elif not your_pattern:
            print("Forgot to enter a pattern!")
        else:
            print("Pass")
# Your pattern here!
pattern = r"\"?([-a-zA-Z0-9.`?{}]+@\w+\.\w+)\"?"
test_email(pattern)
