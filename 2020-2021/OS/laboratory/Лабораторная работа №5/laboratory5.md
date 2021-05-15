---
# Front matter
lang: ru-RU
title: "Лабораторная работа №5"
subtitle: "Дисциплина: операционные системы"
author: "Бирюкова Анастасия Анатольевна"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: lualatex
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы:
приобретение практических навыков общения с системой на уровне командной строки.
# Задание
1. Определите полное имя вашего домашнего каталога. Далее относительно этого каталога будут выполняться последующие упражнения.
2. Выполните следующие действия:
2.1. Перейдите в каталог /tmp.
2.2. Выведите на экран содержимое каталога /tmp. Для этого используйте команду ls с различными опциями. Поясните разницу в выводимой на экран
информации.
2.3. Определите, есть ли в каталоге /var/spool подкаталог с именем cron?
2.4. Перейдите в Ваш домашний каталог и выведите на экран его содержимое.
Определите, кто является владельцем файлов и подкаталогов?
3. Выполните следующие действия:
3.1. В домашнем каталоге создайте новый каталог с именем newdir.
3.2. В каталоге ~/newdir создайте новый каталог с именем morefun.
3.3. В домашнем каталоге создайте одной командой три новых каталога с именами letters, memos, misk. Затем удалите эти каталоги одной командой.
3.4. Попробуйте удалить ранее созданный каталог ~/newdir командой rm. Проверьте, был ли каталог удалён.
3.5. Удалите каталог ~/newdir/morefun из домашнего каталога. Проверьте,
был ли каталог удалён.
4. С помощью команды man определите, какую опцию команды ls нужно использовать для просмотра содержимое не только указанного каталога, но и подкаталогов, входящих в него.
5. С помощью команды man определите набор опций команды ls, позволяющий отсортировать по времени последнего изменения выводимый список содержимого
каталога с развёрнутым описанием файлов.
6. Используйте команду man для просмотра описания следующих команд: cd, pwd,
mkdir, rmdir, rm. Поясните основные опции этих команд.
7. Используя информацию, полученную при помощи команды history, выполните
модификацию и исполнение нескольких команд из буфера команд.

# Выполнение лабораторной работы
1. Узнали полное имя домашнего каталога(Рис.1)
![Picture1](/Users/asyabiryukova/Desktop/Скрины 5 лаба/1.png)

2. Выполнили следующие действия:
Перешли в каталог /tmp(Рис.2)
![Picture2](/Users/asyabiryukova/Desktop/Скрины 5 лаба/2.png)
Посмотрели содержимое каталога /tmp. Для этого используем команду /ls с различными опциями.
Чтобы вывести на экран подробную информацию о файлах и каталогах, необходимо использовать опцию l(Рис.3)
![Picture3](/Users/asyabiryukova/Desktop/Скрины 5 лаба/3.png)
Для того, чтобы отобразить имена скрытых файлов, необходимо использовать команду ls с опцией a(Рис.4)
![Picture4](/Users/asyabiryukova/Desktop/Скрины 5 лаба/4.png)
Определили, принадлежит ли подкаталог cron каталогу /var/spool(Рис.5)
![Picture5](/Users/asyabiryukova/Desktop/Скрины 5 лаба/5.png)
Определили, кто является владельцем файлов и подкаталогов(Рис.6)
![Picture6](/Users/asyabiryukova/Desktop/Скрины 5 лаба/6.png)

3. Выполнили следующие действия:
Создали новый каталог с именем newdir в домашнем каталоге(Рис.7)
![Picture7](/Users/asyabiryukova/Desktop/Скрины 5 лаба/7.png)
В каталоге ~/newdir создали новый каталог с именем morefun(Рис.8)
![Picture8](/Users/asyabiryukova/Desktop/Скрины 5 лаба/8.png)
Создали три новых каталога с именами letters, memos, misk в нашем домашнем каталоге одной командой(Рис.9)
![Picture9](/Users/asyabiryukova/Desktop/Скрины 5 лаба/9.png)
Удалили эти каталоги одной командой(Рис.10)
![Picture10](/Users/asyabiryukova/Desktop/Скрины 5 лаба/10.png)
Попробовали удалить каталог ~/newdir командой rm.(Рис.11) Данный каталог не получилось удалить.
![Picture11](/Users/asyabiryukova/Desktop/Скрины 5 лаба/11.png)
Удалили каталог ~/newdir/morefun из вашего домашнего каталога. Проверили, действительно ли каталог был удалён.(Рис.12)
![Picture12](/Users/asyabiryukova/Desktop/Скрины 5 лаба/12.png)

1. С помощью команды man определили какая опция команды ls позволяет просматривать не только содержимое указанного каталога, но и подкаталогов, входящих в него. Рис 13-18
![Picture13](/Users/asyabiryukova/Desktop/Скрины 5 лаба/13.png)
![Picture14](/Users/asyabiryukova/Desktop/Скрины 5 лаба/14.png)
![Picture15](/Users/asyabiryukova/Desktop/Скрины 5 лаба/15.png)
![Picture16](/Users/asyabiryukova/Desktop/Скрины 5 лаба/16.png)
![Picture17](/Users/asyabiryukova/Desktop/Скрины 5 лаба/17.png)
![Picture18](/Users/asyabiryukova/Desktop/Скрины 5 лаба/18.png)
Нужная опция "-R". Опция -R команды ls позволяет просматривать не только содержимое указанного каталога, но и подкаталогов, входящих в него.

5. Определили при помощи команды man, какой набор опций команды ls позволяет отсортировать выводимый список, с развернутым описанием файлов, по времени последнего изменения. (Рис.19)
![Picture19](/Users/asyabiryukova/Desktop/Скрины 5 лаба/20.png)

1. Использовали команду man, для просмотра описания следующих команд: cd, pwd, mkdir, rmdir, rm. Описание данных команд огромно.(Рис.20)
![Picture20](/Users/asyabiryukova/Desktop/Скрины 5 лаба/19.png)
7. Используя информацию, полученную командой history, выполнили модификацию и исполнение нескольких команд из буфера команд.
![Picture21](/Users/asyabiryukova/Desktop/Скрины 5 лаба/21.png)
![Picture22](/Users/asyabiryukova/Desktop/Скрины 5 лаба/22.png)
![Picture23](/Users/asyabiryukova/Desktop/Скрины 5 лаба/23.png)
![Picture24](/Users/asyabiryukova/Desktop/Скрины 5 лаба/24.png)
![Picture25](/Users/asyabiryukova/Desktop/Скрины 5 лаба/25.png)
![Picture26](/Users/asyabiryukova/Desktop/Скрины 5 лаба/26.png)
![Picture27](/Users/asyabiryukova/Desktop/Скрины 5 лаба/27.png)
![Picture28](/Users/asyabiryukova/Desktop/Скрины 5 лаба/28.png)
# Выводы
В этой лабораторной работе мы приобрели практические навыки общения с системой на уровне командной строки (вход и выход, оперативная помощь, работа с буфером команд, организация файловой системы)
