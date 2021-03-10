# Создание удаленного репозитория

Для того, чтобы просмотреть список настроенных удалённых репозиториев, вы можете запустить команду `git remote`. Она выведет названия доступных удалённых репозиториев. 

Для того, чтобы добавить удалённый репозиторий и присвоить ему имя `(shortname)`, просто выполните команду `git remote add <shortname> <url>`.

## Получение изменений из удалённого репозитория

Для получения данных из удалённых проектов следует выполнить:

```
$ git fetch [remote-name]
```

Эта команда забирает данные в ваш локальный репозиторий, но не сливает их с какими-либо вашими наработками и не модифицирует то, над чем вы работаете в данный момент.

Выполнение `git pull`, как правило, извлекает `(fetch)` данные с сервера, с которого вы изначально клонировали, и автоматически пытается слить `(merge)` их с кодом, над которым вы в данный момент работаете.

## Отправка изменений

Когда вы хотите поделиться своими наработками, вам необходимо отправить их в удалённый репозиторий. Команда для этого действия простая: `git push <remote-name> <branch-name>`. Например, следующая команда отправит вашу ветку `master` на сервер `origin`:
```
$ git push -u origin master
```
Эта команда срабатывает только в случае, если вы клонировали с сервера, на котором у вас есть права на запись, и если никто другой с тех пор не выполнял команду `push`. Если вы и кто-то ещё одновременно клонируете, затем он выполняет команду `push`, а после него выполнить команду `push` попытаетесь вы, то ваш `push` точно будет отклонён. Вам придётся сначала получить изменения и объединить их с вашими и только после этого вам будет позволено выполнить `push`.

***

[Назад](./05-add.md) ~~
[Содержание](./readme.md) ~~
[Дальше](./07-branch.md)