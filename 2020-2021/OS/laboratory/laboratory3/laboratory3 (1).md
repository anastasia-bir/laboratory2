---
# Front matter
lang: ru-RU
title: "Лабораторная работа №3"
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

# Цель работы
Целью данной работы является изучение идеологии и применение средств контроля версий.

# Задание
- Сделайте отчёт по предыдущей лабораторной работе в формате Markdown.
- В качестве отчёта просьба предоставить отчёты в 3 форматах: pdf, docx и md (в
архиве, поскольку он должен содержать скриншоты, Makefile и т.д.)


# Выполнение лабораторной работы
1) В первую очередь, создадим учетную запись на https://github.com. (рис.1)
 ![Picture1](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/1.png)

2)	Настроим систему контроля версий git с использованием сервера репозиториев:
Создадим локальный репозиторий. Сначала сделаем предварительную конфигурацию, указав имя и email владельца репозитория(рис 2):
git config --global user.name "Имя Фамилия"
git config --global user.email "work@mail"
![Picture2](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/2.png)
Для последующей идентификации пользователя на сервере репозиториев необходимо сгенерировать пару ключей, используя команду: ssh-keygen -C "Имя Фамилия <work@mail>" (см. рис. 3)
![Picture3](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/3.png)
С помощью команды cat ~/.ssh/id_rsa.pub | xclip -sel clip (Рис.4) скопируем из локальной консоли ключ в буфер обмена и вставляем ключ в появившиеся на сайте поле. Для этого заходим в настройки, выбираем пункт «SSH and GPG keys»(рис.5), далее нажимаем «New SSH key» и вставляем ключ в раздел «key»(Рис.6)
![Picture4](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/4.png)
![Picture5](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/5.png)
![Picture6](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/6.png)
В результате создается ключ:
![Picture7](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/7.png)
Настройка системы контроля версий завершена.

3)	Создаем репозиторий
![Picture8](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/8.png)
Задаем имя «laboratory2» и ставим галочку на пункте «Add a README file». У нас создается репозиторий(рис.9)
![Picture9](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/9.png)
Теперь скачиваем репозиторий на компьютер(Рис.10) с помощью команды: git clone и ссылки на репозиторий
![Picture10](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/10.png)
Далее вводим команду cd laboratory 2, чтобы перейти в этот каталог. Создаем каталог 2020-2021(mkdir 2020-2021) и переходим в него, далее создаем каталог «OS», переходим в него и создаем каталог «laboratory» и тоже переходим в него(Рис.11)
![Picture11](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/11.png)
Делаем первый коммит и выкладываем его на гитхаб
git commit -m "first commit" (Рис.12)
![Picture12](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/12.png)
Создаем файл, используя команду touch h.txt и git add .(Рис.13)
![Picture13](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/13.png)
Затем повторяем команду git commit -m "first commit"
Используя команду git push, отправим все произведенные изменения локального дерева в центральный репозиторий. (Рис.14)
![Picture14](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/14.png)
4)	Первичная конфигурация. Добавим файл лицензии(рис.15). Команда: 
wget https://creativecommons.org/licenses/by/4.0/legalcode.txt -O LICENSE
![Picture15](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/15.png)
Добавляем шаблон игнорируемых файлов. Сначала просмотрим список имеющихся шаблонов: curl -L -s https://www.gitignore.io/api/list (Рис.16)
![Picture16](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/16.png)
Скачиваем шаблон. Я взяла шаблон для С(Рис.17)
Команда: curl -L -s https://www.gitignore.io/api/c >> .gitignore
Затем добавляем новые файлы, используя команду git add .
Выполняем коммит git commit -m "first commit" и отправляем на гитхаб git push.
![Picture17](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/17.png)
5)	Конфигурация git-flow
Для начала инициализируем git-flow 
Git flow init -f
Префикс для ярлыков устанавливаем в v.
![Picture18](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/18.png)
Проверяем, что мы находимся на ветке develop, командой git branch(Рис.19). Создаем релиз с версией 1.0.0
Git flow release start 1.0.0
![Picture19](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/19.png)
Запишем версию(рис.20) 
echo "1.0.0" >> VERSION
Добавим в индекс: git add .
git commit -am 'chore(main): add version'
![Picture20](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/20.png)
Заливаем релизную ветку в основную ветку, используя команду git flow release finish 1.0.0(Рис.21-22)
![Picture21](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/21.png)
![Picture22](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/22.png)
Отправим данные на github
git push --all
git push --tags
(Рис.23)
![Picture23](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/23.png)
Создаем релиз на гитхаб. Открываем «releases», в пункте «Target» выбираем realese/1.0.0).
(Рис.24)
![Picture24](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/24.png)
У нас создается релиз(рис.25)
![Picture25](https://github.com/anastasia-bir/laboratory2/blob/main/2020-2021/OS/laboratory/2laboratory/25.png)


# Выводы
Мы изучили идеологии и применение средств контроля версий.
