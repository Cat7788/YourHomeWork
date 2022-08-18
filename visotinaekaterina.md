# Система контроля версий Git

**git --version**  - Посмотреть установлен ли git? Посмотреть версию программы git

Для настройки Git надо установить имя и емейл пользователя, от лица которого мы будем сохранять файлы в репозиторий:

**git config --global user.name "Cat"** _(имя пользователя)_

**git config --global user.email "abc.com или ma@ya.ru"** _(email пользователя)_

**git config --list** - выводит параметры, в том числе имя и емэйл пользователя/ проверка установили ли настройки

**git init** - создание репозитория - появляется в  теперь отслеживаемой папке папка .git (Репозиторий - это папка, в которой система контроля версий git позволяет отслеживать все изменения, как в структуре папок и файлов, так и в их содержимом)

**git branch** - посмотреть список веток в репозитории

**git branch catalog** - создать новую ветку с именем catalog

**git branch -d catalog** - удалить ветку с именем catalog

**git checkout -b options** -  -b означает, что ветка options новая и ее нужно создать, одновременно переключаемся на эту новую ветку

**git checkout catalog** - переключаемся в ветку  catalog

**git checkout  _первые 4 символа сохранения_** - перейти к одному из прошлых сохранений

**git log** - смотреть всю историю коммитов (их хеши, авторов и комментарии)

**git status** - посмотреть, есть ли изменения и в какой ветке находимся (Красный - новые файлы для репозитория, зеленые - файлы, добавленные в индекс)

**git add .** - добавить изменения в индекс (сделать отслеживаемыми все файлы с изменениями)

**git add namefile** - добавить в индекс namefile

**git commit -m '_комментарий что изменилось на английском_'** - сохранение изменения файла в Git

**git commit --amend -m '...'** - изменить комментарий к коммиту

**git diff** - отличается ли текущий коммит от последнего коммита? - если git ничего не высветит, то отличий нет. Если есть, то с минусом идут удаленные строки, с плюсом добавленные.

**git merge master** - вливаем ветку master  в текущую ветку

**clear** - стереть то, что было в терминале

**git log --graph** - включить графическое отображение веток

**git show** - убедимся, что изм сохранились. Показывает информацию о последнем коммите и его содержимом. Нажимаем на enter - просматриваем все изменения

**q** - выйти из git show

**git clone _путь к удаленному репозиторию_** - клонируем репозиторий с сервера. Вначале работы нужно склонировать репозиторий на свой компьютер (наз. рабочая копия). В дальнейшем при внесении изменений мы сможем отправлять их на удаленный сервер в исходный репозиторий командой git push, поскольку они уже автоматически связаны

**git pull** - затягивает все изменения из центрального удаленного репозитория в свой локальный

**git push** - отправляем изменения в удаленный репозиторий


<br>

# Язык Markdown

## Выделение текста

Для выделения текста курсивом используется символ звездочка или символ нижнего подчеркивания. 

Пример: *Курсив*

Для выделения текста жирным шрифтом используются две звездочки или два нижних подчеркивания.

Пример:  **Жирный текст**  

## Заголовки

Заголовки выделяются с помощью символа #, используется от одного до шести данных символов, которые устанавливаются в начале строки. Количество символов соответствует уровню заголовка.

## Параграфы

Чтобы создать параграф достаточно отделить строки текста одной или более пустой строкой

## Цитаты

Для обозначения цитат используется знак >. Его можно ставить как перед каждой строкой цитаты, так и только перед первой строкой параграфа
>  Пример цитаты

## Списки

Для формирования ненумерованных списков используются такие маркеры, как звездочки, плюсы или дефисы.
* Первый пункт списка
* Второй пункт списка

Для формирования нумерованных списков используются в качестве маркеров числа с точкой.
1. Первый пункт списка
2. Второй пункт списка

## Гиперссылки

Ссылки могут указывать на содержимое как на соседних страницах или на внешних сайтах, так и на той же странице.

Для создания гиперссылки на другую страницу сайта или на сторонний сайт используется текст ссылки в квадратных скобках  и сразу за ним круглые скобки с  URL-адресом внутри - абсолютным URL-адресом для внешних сайтов и относительным для страниц этого же сайта.

[ссылка на статью в википедии](https://ru.wikipedia.org/wiki/Markdown)

Чтобы добавить ссылку на заголовок в текущем файле, используется символ #, за которым следует текст заголовка в нижнем регистре. При этом нужно удалить знаки препинания из заголовка и заменить пробелы дефисами

[перейдем к руководству по программе git](#руководство-по-программе-git)

## Картинки

Добавление картинки имеет следующий синтаксис
![текст](ссылка на картинку), в котором текст будет выводиться, только при условии, если изображение не загрузится, чтобы дать пользователю понять, что должно было отобразиться на картинке

<br>

# Подключение к удаленному репозиторию

## Существует удаленный репозиторий, нет локального (работа над существующим проектом)

1. Копируем путь к удаленному репозиторию из GitHub
2. Переходим в нужную папку на своем компьютере
3. Используем команду **git clone _путь к удаленному репозиторию_**

В дальнейшем при внесении изменений мы сможем отправлять их на удаленный сервер в исходный репозиторий командой git push, поскольку они уже автоматически связаны

## Нет ни удаленного, ни локального репозитория (работа над новым проектом)

1. Создать удаленный репозиторий в GitHub (название обычно пишут по названию проекта через дефис маленькими буквами)

2. Создать в этом репозитории файл:

* Вариант 1. 
    * Это можно сделать нажатием на ссылку creating a new file - создать любой файл и сразу его закоммитить, вписав снизу под фразой commit new file комментарий к комиту. 
    * Или загрузить в репозиторий какой-то файл (uploading an existing file), перетащить файл и сделать коммит, введя комментарий под словами commit changes. Далее удаленный репозиторий переносим на свой компьютер, как рассказано выше.

* Вариант 2. 
    * Создаем в папке на своем компьютере текстовый файл. 
    * Командой git init создаем репозиторий в этой папке.
    * добавляем файл в индекс
    * Выполняем коммит
    * git branch -M master  - не обязательная команда, задать имя базовой ветки в удаленном репозитории
    * git remote add origin путь к удаленному репозиторию - устанавливает в локальном репозитории связку с удаленным
    * git push -u origin master отправляем файл на удаленный сервер, проверяем изменения на сервере

## Есть локальный репозиторий с проектом, но нет удаленного

1. Создать удаленный репозиторий

2. В локальном репозитории ввести команды:
    * git remote add origin путь к удаленному репозиторию - подключение к удаленному репозторию из локального 
    * команда git branch -M master - не обязательна, задать имя базовой ветки в удаленном репозитории
    * git push -u origin master - отправим в удаленный репозиторий всю информацию из локального, автоматически устанавливает связь между локальным и удаленным репозиториями
