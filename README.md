## Описание
Проект представляет собой API для проекта yatube.

Функционал:

* Авторизация по JWT токену

* Сериализация данных для всех моделей проекта (Post, Comment, Group, Follow)

* Обработка GET, POST, PATCH, PUT и DELETE запросов к базе данных проекта Yatube

## Как запустить проект:
1. Клонировать репозиторий и перейти в него в командной строке:
git clone git@github.com:matrosovmn/api_final_yatube.git
cd yatube_api/
2. Cоздать и активировать виртуальное окружение:
py -m venv env
source env/scripts/activate
3. Установить зависимости из файла requirements.txt:
python -m pip install --upgrade pip
pip install -r requirements.txt
4. Выполнить миграции:
py manage.py migrate
5. Запустить проект:
py manage.py runserver

## Примеры
Для доступа к API необходимо получить токен: Нужно выполнить POST-запрос localhost:8000/api/v1/token/ передав поля username и password. API вернет JWT-токеню

Дальше, передав токен можно будет обращаться к методам, например:

/api/v1/posts/ (GET, POST, PUT, PATCH, DELETE)

При отправке запроса передавайте токен в заголовке Authorization: Bearer <токен>

Слово Bearer здесь заменяет слово Token и означает, что за ним следует сам токен.

## Об авторе
Начинающий разработчик Михаил Матросов. С моими другими работами вы можете ознакомится по ссылке: https://github.com/matrosovmn
