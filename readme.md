<<<<<<< HEAD
# Инструкция по работе с git и удаленными репозиториями

## Что такое git?
 ![Git](git.jpg)Git - это распределенная система управления версиями, необходимая для отслеживания и ведения истории изменения файлов. Например в каком нибудь проекте. Git позволяет "откатить" проект до более старой версии, сравнить, проанализировать или слить свои изменения в репозиторий.

*Git* одна из реализаций распределенных систем контроля версий. *Git* на данный момент является самой популярной реализацией. Самой популярной реализацией *Git* является [GitHub](https://github.com)

## Подготовка репозитория
Для того, чтобы создать ренпозиторий используется команда "git init". Для этого необходимо написать в терминале в папке будущего репозитория *git init*

## Создание "сохранений"

Хорошо написанный комментарий к коммиту — это лучший способ рассказать о контексте сделанных изменений другим разработчикам (а также самим себе — в будущем!). Поэтому сообщения к коммиту должны быть лаконичными и однородными. Чтобы не писать команду *git add* каждый раз при сохранений коммита, можно ввести команду *git commit -am <наше сообщение>*.

### Добавление файла к коммиту

Для добавления файла к коммиту используется команда *git add*. Пишется она следующим образом *git add<имя файла>* в терминале в папке с созданным репозиторием.

### Созданеи коммита

Для создания нового "сохранения" используется команда *git commit*. Используется она следующим образом: в терминале с папкой-репозиторием  пишется *git commit -m <сообщение к коммиту>*. Сообщение к коммиту писать **ОБЯЗАТЕЛЬНО**!!! 

## Журнал изменений
Для просмотра журнала изменений используется команда *git log*. Для этого в терминале в папке с репозиторием достаточно написать *git log*

## Перемещение между коммитами
Для перемещения между сохранениями используется команда *git checkout*. Для того, чтобы переместиться на указанный коммит в терминале в папке с репозиторием пишем *git checkout <номер коммита>*. **Номер коммита** берется из журнала изменений, о котором сказано выше. После перемещения на указанный коммит мы попадаем в состояние **detached head**. Чтобы вернуться к обычной работе, необходимо написать *git checkout master*.

## Ветки в git

Для того, чтобы создать новую ветку используется команда **git branch <имя ветки>**. Ветка в Git это подвижный указатель на один из коммитов. Обычно ветка указывает на последний коммит в цепочке коммитов. Важно помнить, что ветка берет свое начало не от ветки, а от последнего коммита который находиться в той ветке, в которой вы находились. Ветки в *Git* нужны, чтобы работать с "чистовиком" и "черновиками". Для того, чтобы создать новую ветку используется команда "git branch". В Терминале папки репозитория, напишите *git branch* <название ветки>.

## Слияние веток и разрешение конфликтов
Для слияния двух веток используется команда *git merge*. Для ее использования необходимо перейти в ту ветку, куда Вы хотите сделать слияние, после чего в терминале в папке с репозиторием написать git merge <название сливаемой ветки>. Чаще всего слияние происходит автоматически, но возможно **КОНФЛИКТЫ**. В таком случае, необходимо вручную получить желаемую версию файла и сделать коммит.

## Удаление веток

Для удаления ветки используется команда *git branch -d <имя ветки>*. Необходимо помнить, что ветка, которую вы удаляете, не должна быть вашей текущей веткой, в которой вы работаете, иначе отобразится ошибка вида:

**error: Cannot delete branch ’mybranch’ checked out at ’/path/to**

Поэтому, если вам нужно удалить текущую ветку, то сначала нужно переключиться на какую-либо другую ветку применив команду *git checkout <имя ветки>*, а только потом выполнять удаление.

Если вдруг возникает ошибка: 

**The branch ’mybranch’ is not fully merged. If you are sure you want to delete it** 

и вы по прежнему хотите удалить ветку, то для принудительного удаления ветки можно воспользоваться опцией -D:

## Получение удаленного репозитория

## Скачивание изменений удаленного репозитория

## Отправка изменненгий в удаленный репозиторий

