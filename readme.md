# Инструкция по работе с git

## Что такое git?
 ![Git](git.jpg)Git - это распределенная система управления версиями, необходимая для отслеживания и ведения истории изменения файлов. Например в каком нибудь проекте. Git позволяет "откатить" проект до более старой версии, сравнить, проанализировать или слить свои изменения в репозиторий.

## Подготовка репозитория
Для того, чтобы создать ренпозиторий используется команда "git init". Для этого необходимо написать в терминале в папке будущего репозитория *git init*

## Создание "сохранений"

### Добавление файла к коммиту

Для добавления файла к коммиту используется команда *git add*. Пишется она следующим образом *git add<имя файла>* в терминале в папке с созданным репозиторием.

### Созданеи коммита

Для создания нового "сохранения" используется команда *git commit*. Используется она следующим образом: в терминале с папкой-репозиторием  пишется *git commit -m <сообщение к коммиту>*. Сообщение к коммиту писать **ОБЯЗАТЕЛЬНО**!!! 

## Журнал изменений
Для просмотра журнала изменений используется команда *git log*. Для этого в терминале в папке с репозиторием достаточно написать *git log*

## Перемещение между коммитами
Для перемещения между сохранениями используется команда *git checkout*. Для того, чтобы переместиться на указанный коммит в терминале в папке с репозиторием пишем *git checkout <номер коммита>*. **Номер коммита** берется из журнала изменений, о котором сказано выше. После перемещения на указанный коммит мы попадаем в состояние **detached head**. Чтобы вернуться к обычной работе, необходимо написать *git checkout master*.

## Ветки в git

Для того, чтобы создать новую ветку используется команда **git branch <имя ветки>**. Ветка в Git это подвижный указатель на один из коммитов. Обычно ветка указывает на последний коммит в цепочке коммитов. Важно помнить, что ветка берет свое начало не от ветки, а от последнего коммита который находиться в той ветке, в которой вы находились. 

## Слияние веток и разрешение конфликтов

## Удаление веток

Чтобы удалить ветку используется команда git branch -d