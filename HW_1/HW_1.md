# HW_1. The first part
# Linux terminal (GitBash) commands

___

Нужно уметь делать все пункты задания.
Куда и в каком виде отправлять задание - скажу позже.

1) Посмотреть где я
2) Создать папку
3) Зайти в папку
4) Создать 3 папки
5) Зайти в любоую папку
6) Создать 5 файлов (3 txt, 2 json)
7) Создать 3 папки
8. Вывести список содержимого папки
9) + Открыть любой txt файл
10) + написать туда что-нибудь, любой текст.
11) + сохранить и выйти.
12) Выйти из папки на уровень выше
—
13) переместить любые 2 файла, которые вы создали, в любую другую папку.
14) скопировать любые 2 файла, которые вы создали, в любую другую папку.
15) Найти файл по имени
16) просмотреть содержимое в реальном времени (команда grep) изучите как она работает.
17) вывести несколько первых строк из текстового файла
18) вывести несколько последних строк из текстового файла
19) просмотреть содержимое длинного файла (команда less) изучите как она работает.
20) вывести дату и время
=========

Задание *
1) Отправить http запрос на сервер.
http://162.55.220.72:5005/terminal-hw-request
2) Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13

=====================
1) Посмотреть где я - pwd
2) Создать папку - mkdir foldername
3) Зайти в папку - cd foldername

___
# Решение
___

### 1. Посмотреть где я

```bash
pwd
```
### 2. Создать папку

```bash
mkdir foldername
```
### 3. Зайти в папку

```bash
cd foldername
```
### 4. Создать 3 папки

```bash
mkdir foldername_1 foldername_2 foldername_3
```

### 5. Зайти в любоую папку

```bash
cd foldername_1
```

### 6. Создать 5 файлов (3 txt, 2 json)

```bash
touch file_1.txt file_2.txt file_3.txt file_1.json file_2.json
```

or create five files throught cat 

```bash
cat > file_1.txt file_2.txt file_3.txt file_1.json file_2.json
```

### 7. Создать 3 папки

```bash
mkdir folder_1 folder_2 folder_3
```

### 8. Вывести список содержимого папки

```bash
ls -la
```

без скрытых папок

```bash
ls -l
```

### 9. Открыть любой txt файл

```bash
vim file_1.json
```

### 10. Написать туда что-нибудь, любой текст.

```
{
        "year":         2022,
        "name":         "Andrei",
        "active":       True,
        "skills":       ["Python", "Postman", "JS"]
}
```

### 11. Сохранить и выйти.

```bash
Esc
:wq
```

### 12. Выйти из папки на уровень выше

```bash

cd ../
```

### 13. Переместить любые 2 файла, которые вы создали в любую другую папку.

```bash
mv foldername_1/file_1.json foldername_1/file_1.txt foldername_2
```

### 14. Скопировать любые 2 файла, которые вы создали в любую другую папку.

```bash
cp foldername_1/file_2.json foldername_1/file_2.txt folder_2
```

### 15. Найти файл по имени

```bash
find foldername_1/file_3.txt
```

### 16. Просмотреть содержимое в реальном времени (-f - обновлять информацию по мере появления новых строк в файле)

```bash
tail -F file_1.json
```
Поиск конкретного термина при мониторинге файла

```bash
tail -f file_1.json | grep search_term
```
### 17. Вывести несколько первых строк из текстового
файла

```bash
head -n3 file_1.json
```

```
{
	"year":		2022
	"name": 	"Andrei",
```

### 18. Вывести несколько последних строк из текстового файла

```bash
tail -n3 file_1.json
```
```
	"active": 	True,
	"skills":	["Python", "Postman", "JS"]
}
```

### 19. Просмотреть содержимое длинного файла
 (команда less) изучите как она работает.

```bash
less long_file.json
q
```

### 20. Вывести дату и время

```bash
date
```

-----

1. Отправить http запрос на сервер.
http://162.55.220.72:5005/terminal-hw-request

```bash
$ curl "http://162.55.220.72:5005/terminal-hw-request"

```
В консоле получен ответ на запрос;

```bash
 % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   283  100   283    0     0   2916      0 --:--:-- --:--:-- --:--:--  2947{
  "Intro": "Hello!! This is your the first response from server",
  "Tasks": {
    "Task_1": "Send the next URL in terminal: http://162.55.220.72:5005/get_method?name=(set_your_String)&age=(set_your_number)",
    "result": [
      "Your_String",
      "Your_number"
    ]
  }
}

```
В задании оказалось подзадание отправить свои данные на сервер методом Get:

```bash
bra75@DESKTOP-HH0SRPU MINGW64 ~
$ curl 'http://162.55.220.72:5005/get_method?name=Andrei&age=47'
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100    24  100    24    0     0    241      0 --:--:-- --:--:-- --:--:--   244[
  "Andrei",
  "47"
]


bra75@DESKTOP-HH0SRPU MINGW64 ~
$

```

2. Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13

```bash

#2) Написать скрипт который выполнит
#автоматически пункты 3, 4, 5, 6, 7, 8, 13

mkdir foldername_1

#3) Зайти в папку
cd foldername_1

#4) Создать 3 папки
mkdir foldername_1 foldername_2 foldername_3

#5) Зайти в любоую папку
cd foldername_1

#6) Создать 5 файлов (3 txt, 2 json)
touch file_1.txt file_2.txt file_3.txt file_1.json file_2.json

#7) Создать 3 папки
mkdir foldername_1 foldername_2 foldername_3

#8). Вывести список содержимого папки
ls

#13) переместить любые 2 файла, которые вы создали,
#	 в любую другую папку.
mv file_1.json file_1.txt ../foldername_2
```

После выполнения скрипта в папке "QA 30 Group" были созданы три папки в первой  foldername_1 вновь  созданы 3 папки и 5 файлов три с расширением txt и два с джейсонками, далее два файла были перенесены в папку foldername_2.

### Видео по запуску нижеуказанного скрипта из под консоли Bash можно посмотреть [здесь](https://youtu.be/hMTNlvl1HnE)


```bash
bra75@DESKTOP-HH0SRPU MINGW64 /d/QA 30 Group
$ 
#!/bin/bash
#2) Написать скрипт который выполнит
#автоматически пункты 3, 4, 5, 6, 7, 8, 13

mkdir foldername_1

#3) Зайти в папку
cd folder_1

#4) Создать 3 папки
mkdir foldername_1 foldername_2 foldername_3

#5) Зайти в любоую папку
cd foldername_1

#6) Создать 5 файлов (3 txt, 2 json)
touch file_1.txt file_2.txt file_3.txt file_1.json file_2.json

#7) Создать 3 папки
mkdir foldername_1 foldername_2 foldername_3

#8). Вывести список содержимого папки
ls

#13) переместить любые 2 файла, которые вы создали,
mv file_1.json file_1.txt ../foldername_2
bash: cd: folder_1: No such file or directory
mkdir: cannot create directory ‘foldername_1’: File exists
file_1.json  file_2.json  file_3.txt     foldername_2/
file_1.txt   file_2.txt   foldername_1/  foldername_3/

bra75@DESKTOP-HH0SRPU MINGW64 /d/QA 30 Group/foldername_1
$

```
<img width="1080" alt="авторизация" src="https://github.com/AndreiBra/BASH_Console_Commands/blob/main/HW_1.png">

