# Home_Work


# Что такое git
 *Это система контроля версий*

# Подготовка репозитория
 * git config --global user.email
 * git config --global user.name

 Прописать пользователя локально
 * git config --local ...

# Создание "Сохранений"
*Редактируем файл, после чего добавляем этот файл для отслеживания командой add и фиксируем наши изменения командой commit*

## git add
*Добавляет файлы, которые нужно отслеживать*

команды:
* git add name_of life

    Добавляет файл  с именем name_ of life
* git add .

    Добавляет все файлы

    *Фиксируем наши изменения*
Команды:
* git commit -m "message"


    Фиксируем изменения и добавляем к нему сообщение
* git commit -a -m "message"

    Фиксируем изменения всех файлов и добавляем к нему сообщение

# Перемещение между сохранениями
*Перемещение между коммитами*

* git checkout commit_code
commit_code - код коммита, который можно получить из git log

*Вернуться к актуальному состоянию*
* git checkout master

# Состояние репозитория:

## git status
*проверяем состояние нашего репозитория*

## git diff
*Посмотреть разницу между текущими изменениями и тем что закомичены*

## git show
*Показывает изменения внесенные в последнем комите*

## git show commit_name
*Показывает изменения внесенные в коммите с именем commit_name*

# Журнал изменений
*Показать все наши изменения:*
* git log
*Показать все наши изменения с визуализацией веток:*
* git log --graph

# Ветки в git
*Создание новой ветки:*
* git branch branch_name

*Вывести список всех веток:*
* git branch

*Переход к ветке:*
* git checkout branch_name

# Слияние веток и решение конфликтов 1
*Команда для слияния:*
* git merge

*В случае, если merge, вызовет конфликт, то нужно в ручную посмотреть изменения в файлах и убрать лишние. После чего сделать коммит с этими правками.*

# Удаление веток
*Команда:*
* git branch -d branch_name

# Справка
Модификатор команд, который выведет информацию о той команде, к которой был применён
Примеры:
* git commit --help
* git status --help


# Инструкция по работе  с git
1. Прописать пользователя
    * git config --global user.email
    * git config --global user.name
2. Создать репозиторий
    * git init
3. Работа с репозиторием
    1. Изменение файлов и их сохранение:
        * git add
        * git commit
    2. Информация о состоянии репозитория:
        * git status
        * git log
        * git diff


# Cписок команд

## git init
*Команда, которая создаёт наш репозиторий*

## git status
*Проверяем состояние нашего репозитория*

## git add
*Добавляет файлы, которые нужно отслеживать*

команды:
* git add name_of life

    Добавляет файл  с именем name_ of life
* git add .

    Добавляет все файлы

## git commit
*Фиксируем наши изменения*
Команды:
* git commit -m "message"


    Фиксируем изменения и добавляем к нему сообщение
* git commit -a -m "message"

    Фиксируем изменения всех файлов и добавляем к нему сообщение


## git log
*Показывает все наши изменения*

## git checkout
*Переход к одному из комитов*

## git checkout master
*Вернуться к актуальному состоянию и продолжить работу*

## git diff
*Посмотреть разницу между текущими изменениями и тем что закомичены*

## --info
*Модификатор команд, который выведет информацию о той команде, которой был применён*
Примеры:
* git commit --info
* git status --info

# Создание удаленного репозитория

Команды:
* git init {имя проекта}

   Создает новый локальный репозиторий
* git clone {url}

   Скачать репозиторий
   # Проверка состояния репозитория
       * git diff

           Изменения в ещё не  добавленных в индекс файлов
       * git diff --cached

           Изменения в уже добавленных
       * git diff HEAD

           Все изменения
       * git diff hash1 hash2
           
           Изменения между двумя компонентами
       * git blame {имя файла}
           
           Получить даты изменений и их авторов
       * git show hash:file

           Получить список изменений файла в определённом коммите
       * git log
           
           Список коммитов
       * git log -p {файл или папка}

           Показать историю изменений, включая  диффы
    # Обновление
       * git fetch
           
           Скачать изменения из удаленного репозитория
       * git pull
           
           Скачать изменения из удаленного репозитория и смержить
       * git pull --rebase

           Скачать изменения из удаленного репозитория и наложить незапушенные коммиты поверх скачанных
       * git push

            Отправить локальные коммиты в удаленный репозиторий 