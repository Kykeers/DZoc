# Honework file

# Инструкция для работы с Git

## Что такое Git?
Git - это одна из реализаций распределённых систем контроля версий, имеющая как локальные, так и удалённые репозитории. Является самой популярной реализацией систем контроля версий в мире.

## Настройка
Настройка нужна для того, чтобы указывался автор commita.
Установим имя для вашего пользователя
Вместо <ваше_имя> можно ввести, например, Grisha_Popov
Кавычки оставляем
*git config --global user.name "<ваше_имя>"*

Теперь установим email. Принцип тот же.
*git config --global user.email "<адрес_почты@email.com>"*

## Подготовка репозитория
Для создания рупозитория необходимо выполнить команду *git init*  в папке с репозиторием появится скрытая папка .git

## Создание коммитов

### Git add
Для добавления изменений в коммит используется команда *git add*. Чтобы её использоватть следует ввести *git add <имя файла>*

### Просмотр состояния репозитория
Для того, чтобы посмотреть состояние репозитория используется команда *git status*

### Создание коммитов
Для того, чтобы создать коммит(сохрание) необходимо выполнить команду *git commit*. Выполняется она так: *git commit -m "комментарий к коммиту"*

## Работа с ветками

Ветка - это набор commit (кружок), которые идут друг за другом. У ветки есть название, основную ветку чаще всего называют master (на картинках будет называться main) . Если говорить простыми словами, то ветка master - это наш проект.

Другие ветки - это отдельное место для реализации нового функционала или исправление багов (ошибок) нашего проекта. То есть, с отдельной веткой вы делаете что угодно, а затем сливаете эти изменения в основную ветку master

### Создание ветки
Для того, чтобы создать новую ветку можно использовать две команды *git checkout* или *git branch*. Выполняются они так *git branch <название_ветки>* и *git checkout -b <название_ветки>*

### Переключение между ветками
Для того, чтобы переключиться между ветами нужно использовать команду *git checkout*. Выполняется она так *git checkout <название_ветки>*

### Слияние веток (в master)
Для этого нужно переключиться в ветку master и выполнить следующую команду:\

1. Переключаемся в master
*git checkout master*

2. Обновляем локальную ветку с сервера
git pull origin master

Делаем merge вашей ветки, в ветку в которой вы находитесь
В данном примере это master
*git merge <название_ветки>*

❗️ Перед тем как сливать новый merge , стоит обновить локальную ветку master , во избежания дальнейших проблем.

Команда merge берет все изменения из ветки (например bugFix) и добавляет их в ветку master.

После того как вы слили все изменения в master , нужно отправить их в GitHub. Для этого обязательно нужно находиться в ветке master :

*git checkout master*

3. Отправляем наши изменения в GitHub
*git push origin master*
Теперь все ваши изменения, в ветке master улетели в GitHub. Таким же образом, можно отправить любую другую ветку:

*git checkout <название_ветки>*
*git push origin <название_ветки>*

? Совет. Каждый коммит, лучше заливать сразу в удаленный репозиторий. Никто не застрахован, поломки собственного ПК. Поэтому чтобы не потерять все наработки, не забывайте сливать ваши изменения на GitHub.

## Клонирование проекта
*git clone <адрес проекта>*

