# Работа с ветками командой git branch

__Перемещение по веткам__
``` sh
git checkout <название ветки куда надо перейти>
```

__Отображение всех веток - это__
``` sh
git branch
```

__Создание новой ветки__
```sh
git branch <название _новой_ветки>
```

__Удаление ветки__ 
```sh
git branch -d <название_ветки>
```
__Сляиние ветвей__
```sh
git merge <Название той ветки, которую хотим слить в главную ветку>
```
 _**Если появился конфликт , решить его вручную**_


# Просмотр д-й, журнала

* __git log__               Большой просмотр (выход из режима q)
* __git log__ --oneline --graph   Просмотр одной строкой



# *Другие команды*

__Cохранение файла:__
```sh
ctrl+s
git add <название файла.md> 
```

__Добавление коммита описания д-ия:__
```sh
git commit -m "Комментарий что именно сделали"
```


# Инструкция для работы с Markdown

## Выделение текста

Чтобы выделить текст курсивом нужно обрамить его (*), или знаком нижнего подчеркивания (_). 
*Вот так*, или _вот так_

 Чтобы выделить полужирным - двойные **. Или двойное нижнее подчеркиваение
**Вот так**, или __вот так__

``` sh
Альтернативные способы выделения текста жирным или курсивом для того чтобы совмещать два этих способа. 

Например 
```
_**вот так**_

## Списки
Чтобы  выделить ненумерованный список использ , нарпимер (*)

## Работа с изображениями

Чтобы вставить изобр в текст, достаточно написать:


![Это Симпсоны](13.jpg)
![eto_ewe_kartinka](leo.jpg)

Чтобы выделить текст курсивом нужно обрамить его *.
*Вот так*

 Чтобы выделить полужирным - двойные **.
**Вот так**

* git add и имя файла - это добавить файл
* git commit -m "Пишем то что добавили, сделали" - сохраняем файл


## Списки

Чтобы добавить ненумерованый списки необх пункты выделить (*), или знаком +. Например, вот так:
* Элемент 1
* Элемент 2
+ Элемент 3

Чтобы добавить нумерованные списки, пункты просто нумеруем.
Например, вот так:

1. Пункт
2. Пункт

## Рабоnа с изображениями

## Ссылки

## Таблицы

## Цитаты

# Начало работы 

## clear- очищаем терминал

*Созадем папку, создаем файл, подписывает файл с расширением*

* git init - инициализируем репозиторий

* git status-  проверяем статус репозитория

* git add назв ветки - добавляем файл в репозиторий

* git log - смотрим коммиты с текстом комментариями (Выйти из этого осстояния q)

```sh
# git branch - ветки репозитория просто смотреть какие есть и на какой находимся. Если пишем ее название, то созадем новую ветку.

 # git checkout и название ветки на какую хотим перемиститься.

```

* git merge и указываем ту ветку которую необх сюда добавить.

ПОТОМ

 * git branch -d назв. удаляемой ветки (Если поставить D то удалит даже, если не было слияния ветвей)

 
* git add название файла - добавляем файл в репозиторий
 
* git log - журнал коммитов, что добавили 

```sh
# git branch - ветки репозитория просто смотреть какие есть и на какоц находимся. Если пишем ее название то созадем новую ветку.

# git checkout и название ветки на какую хотим перемиститься.

```
git log --graph - Показывает графически как сливались ветки.

## Чтобы создать ветку пишем 
```sh
git branch [назв_ветки]
```
# Работа с Git Hub

Копируем в гит хабе чужой репозиторий и в терминале через команду
* git clone [скопированная ссылка чужого репозитория]
* git cd [пишем адрес названия папки чужого репозитория]
* git status  и всё должно показывать нормально.

# Команды с теста с семинара 

* git pull cкачать данные с репозитория
* git diff увидеть разницу между версиями
* git clone локальная копия удаленного репозитория


# Это репозиторий для обучения pull request

## Первые шаги

1. Делаем fork репозитория, в которой потом хотим сделать pull request. Ищем кнопку Fork на странице репозитория <https://git@github.com:gulden-geekbrains/version_control.git>
2. Выполняем команду клонирования из своей fork-копии
```sh
git clone git@github.com:*YOURE_GITHUB*/version_control.git
```
3. Создаем новую ветку и вносим необходимые изменения в файл
```sh
git checkout -b updatereadme
vim README.md
git add README.md
git commit -m "Добавили инструкцию как создать pull request"
```
4. Делаем push  
```sh
git push --set-upstream origin updatereadme
```
5. Переходим на свою страницу репозитория. Выбираем ветку **updatereadme** и жмем кнопку **Compare & pull request**

## Заметки

Что бы сделать push от другого пользователя необходимо выполнить команду
```sh
GIT_SSH_COMMAND='ssh -i ~/.ssh/user-private-key -o IdentitiesOnly=yes' git push git@github.com:gulden-geekbrains/version_control.git
```

вместо *user-private-key* подставьте свой ключ

Можно прописать настройки для подсоединения по ssh
```sh
git config remote.origin.url git@github.com:gitusername/reponame
git config core.sshCommand "ssh -i ~/.ssh/user-private-key -o IdentitiesOnly=yes"
```
# Как подружить git с github под Windows 10

Вот видео инструкция https://youtu.be/E8cIjbJMEpE
## Эта видео инструкция не открывается   ^

**git branch -M main**  (Переименовать ветку на которой находимся)
  Добавили текст 

  Добавили текст локально

  git pull  отправляем изменения из своего гита в гитхаб

  Добавление текста через браузер редактор.
