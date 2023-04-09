## Описание
Проект представляет собой API для проекта Yatube.

Функционал:

* Авторизация по JWT токену;

* Возможность создавать посты и комментарии к ним;

* Подписываться на авторов;

* Создавать группы;

* Обработка CRUD запросов к базе данных проекта Yatube.


## Как запустить проект:
1. Клонировать репозиторий и перейти в папку (каталог) в командной строке:
```
git clone git@github.com:matrosovmn/api_final_yatube.git
```
```
cd yatube_api/
```
2. Cоздать и активировать виртуальное окружение:
```
python -m venv venv
```
```
source venv/Scripts/activate
```
3. Установить зависимости из файла requirements.txt:
```
python -m pip install --upgrade pip
```
```
pip install -r requirements.txt
```
4. Выполнить миграции:
```
python manage.py migrate
```
5. Запустить проект:
```
python manage.py runserver
```


## Примеры
Для доступа к API необходимо получить токен: 

Нужно выполнить POST-запрос localhost:8000/api/v1/token/ передав поля username и password. 
API вернет JWT-токен.

Дальше, передав токен можно будет обращаться к методам, например:

/api/v1/posts/ (GET, POST, PUT, PATCH, DELETE)

При отправке запроса передавайте токен в заголовке Authorization: Bearer <токен>

Слово Bearer здесь заменяет слово Token и означает, что за ним следует сам токен.

Подробные примеры запросов можно посмотреть по [ссылке](http://127.0.0.1:8000/redoc/) после запуска сервера с проектом.


## Об авторе
Начинающий разработчик Михаил Матросов. С моими другими работами вы можете ознакомится по ссылке: https://github.com/matrosovmn


![Jokes Card](https://readme-jokes.vercel.app/api)
