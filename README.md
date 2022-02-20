
# Работа с Git

## 1. Проверка наличия установленного Git
В терминале выполнить команду `git version`.
Если Git установлен, появится сообщение с информацией о версии программы. Иначе будет сообщение об ошибке.

## 2. Установка Git
Загружаем последнюю версию Git с сайта 
https://git-scm.com

## 3. Настройка Git
При первом использовании Git необходимо представиться. Для этого нужно ввести в терминале две команды:
```
git konfig --global user.name "Ваше имя"
git konfig --global user.email "email@example.com"
```
## 4. Создание репозитория Git
Для того, что бы Git смог отслеживать изменения фала, необходимо инициализировать репозиторий. в терминале ввести команду `git init`. После инициализации создается специальная скрытая папка для Git.

## 5. Запись изменений в репозиторий
Для фиксирования изменений в репозиторий Git используются следующие команды:
* `git status` - просмотреть статус нужного репозитория
* `git add` - добавляет файл к отслеживаемым, а так же фиксирует изменения содержимого файла для последующего коммита 
* `git commit -m " "` - зафиксировать состояние изменений

_**В кавычках вводится поясняющий комментарий**_
* `git diff` - просмотреть список изменений
Показывает непосредственно добавленные и удаленные строки.
1. git diff - не внесенные изменения
2. git diff /первые четыре цифры коммита/ /первые четыре цифры коммита/ - изменения между указанными коммитами
## 6. Просмотр истории коммитов
Для того, что бы увидеть все коммиты, необходимо ввести команду `git log`. При этом для каждого коммита выводятся следующие данные:
 * хэш
 * автор
 * дата
 * сообщение
 
 *Для более короткого вывода коммитов надо набрать команду `git log --oneline`*

## 7. Перемещение между коммитами
Для того что бы перемещаться между коммитами используется команда `git checkout " "`. В кавычках вводится номер коммита.
Для возврата в актуальное состояние необходимо запустить команду `git checkout master`

**Достаточно ввести первые четыре символа из номера коммита**

## 8. Игнорирование файла
1. Создать файл `.gitignore`
2. В файле `.gitignore` указать имя файлов для игнорирования.

*Сохранить!*

3. Добавить файл для ослеживания командой `git add .gitignore`
4. Закомитить командой `git commit -m ""`

## 9. Работа с ветками
### 1. Создание новых веток
Новая ветка создается командой `git branch /имя ветки/`. 
 Команда `git branch` показывает весь список имеющихся веток. Знак * указывает на какой ветке находимся.
 ### 2. Слияние веток
 Для слияния веток необходимо запустить команду `git merge /имя ветки/`. Команда вызывается из той ветки, в которую надо залить ветку /имя ветки/.
 ### 3. Разрешение конфликтов
 При слиянии веток возможно возникновение конфликтов: изменения удаляют или изменяют существующую информацию.
 Для решения конфликта есть следующие варианты:
 * выбрать имеющуюся версию
 * выбрать версию, вливаемую по merge
 * выбрать два варианта
 * сравнить оба варианта
 
 После разрешения конфликта результат необходимо сохранить и закоммитить.
 
### 4. Удаление ветки
Для удаления ветки выполнить команду `git branch -d /имя ветки/`.

При удалении не слитых веток появится ошибка. Если действительно необходимо удалить ветку со всеми наработками, использовать команду `git branch -D /имя ветки/`.

## 10. Работа с удаленными репозиториями

* 10.1 Основные команды

Для работы с удаленными репозиториями необходимо зарегестрироваться на сервисе (например GitHub).
* команда `git clone /ссылка/` создает локальную копию удаленного репозитория
* команда `git pull` скачивает изменения с удаленного репозитория в локальный, автоматически делая merge 
* команда `git push` отправляет локальный репозиторий на внешний. 

*Необходима авторизация!*

* 10.2 Добавление своих изменений в чужой репозиторий (pull request)


* В своём аккаунте на GitHub создать копию репозитория /имя чужого репозитория/ с помощью кнопки **"Fork"**.

* Клонировать копию репозитория на локальный компьютер.

* Создать новую ветку.

* Добавить свои изменения в новую ветку.

* Зафиксировать изменения (коммиты).

* Отправить изменения на GitHub.

* На сайте GitHub выполнить **Pull request**.


