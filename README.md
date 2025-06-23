### Прохождение OverTheWire Bandit LVL 🚀

🕹️ OverTheWire Bandit — это популярный онлайн-игровой сервер для обучения основам Linux и информационной безопасности. Он предназначен для начинающих и позволяет освоить базовые команды Linux, работу с файлами, правами доступа, сетевыми инструментами и криптографией в интерактивном формате.

🔑 Level 6 → Level 7 (bandit6)

Задача: Найти файл где-то на сервере, принадлежащий пользователю bandit7, группе bandit6, размером 33 байта.

Подключение:

    bash

    ssh bandit6@bandit.labs.overthewire.org -p 2220  

    Пароль: DXjZPULLxYr17uwoI01bNLQbtFemEgo7

Поиск и чтение файла:
 
    bash

    find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null

    find / – поиск по всей системе.

    -user bandit7 – владелец bandit7.

    -group bandit6 – группа bandit6.

    -size 33c – размер 33 байта.

    2>/dev/null – скрываем ошибки "Permission denied".


🚩 Флаг (Пароль для bandit7): morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

🔑 Level 7 → Level 8 (bandit7)

Задача: Найти пароль в файле data.txt рядом со словом millionth.

Подключение:

    bash

    ssh bandit7@bandit.labs.overthewire.org -p 2220  

    Пароль: HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

Поиск пароля:

    bash

    cat data.txt | grep millionth

    grep '' - поиск по указанному слову.

🚩 Флаг (Пароль для bandit8): dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

🔑 Level 8 → Level 9 (bandit8)

Задача: Найти строку, встречающуюся один раз в файле data.txt.

Подключение:

    bash

    ssh bandit8@bandit.labs.overthewire.org -p 2220  

    Пароль: cvX2JJa4CFALtqS87jk27qwqGhBM9plV

Решение:
    
    bash

    sort data.txt | uniq -u

    sort – сортирует строки.

    uniq -u – выводит только уникальные строки.

🚩 Флаг (Пароль для bandit9): 4CKMh1JI91bUIZZPXDqGanal4xvAg0JMR

🔑 Level 9 → Level 10 (bandit9)

Задача: Найти строку в файле data.txt, которой предшествует несколько "=".

Подключение:

    bash

    ssh bandit9@bandit.labs.overthewire.org -p 2220  

    Пароль: UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR

Решение:

    bash

    strings data.txt | grep "==="

    strings – извлекает читаемые строки из бинарного файла.

    grep "===" – ищет строки с ===.

🚩 Флаг (Пароль для bandit10): FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey

🔑 Level 10 → Level 11 (bandit10)

Задача: Декодировать base64 в файле data.txt.

Подключение:

    bash

    ssh bandit10@bandit.labs.overthewire.org -p 2220  

    Пароль: truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk

Декодирование:

    bash

    cat data.txt | base64 -d

    base64 -d - открываем файл в кодировке base64.

🚩 Флаг (Пароль для bandit11): dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

🔑 Level 11 → Level 12 (bandit11)

Задача: Декодировать ROT13 в файле data.txt.

Подключение:

    bash

    ssh bandit11@bandit.labs.overthewire.org -p 2220  

    Пароль: IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR

Решение:

    bash

    cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'

    tr – заменяет символы по схеме ROT13.

🚩 Флаг (Пароль для bandit12): 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu

🌑 В скором времени будет выложен репозиторий с прохождением 12-18 lvl.
