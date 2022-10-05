# Yatube API
![Python version](https://img.shields.io/badge/python-3.7-yellow) ![Django version](https://img.shields.io/badge/django-2.2-orange)

API на основе сообщества [Yatube](https://github.com/AleksandrUsolcev/hw05_final)

## Технологии
- Python 3.7+
- [django](https://github.com/django/django) 2.2.16
- [django-rest-framework](https://github.com/encode/django-rest-framework) 3.12.4
- [Simple JWT](https://github.com/jazzband/djangorestframework-simplejwt) 4.7.2
- [djoser](https://github.com/sunscrapers/djoser) 2.1.0

## Запуск проекта в dev-режиме
Клонировать репозиторий
Установить и активируйте виртуальное окружение
```
python3 -m venv venv

# Активация окружения для Mac или Linux:
source venv/bin/activate 
# и для Windows:
source venv/Scripts/activate 
``` 
Установить зависимости из файла requirements.txt
```
pip install -r requirements.txt
``` 
Выполнить миграции и запустить проект
```
python3 manage.py migrate
python3 manage.py runserver
``` 
## Получение персонального токена
Для взаимодействия с API необходимо завести учетную запись пользователя, 
или суперпользователя и иметь персональный токен
```
python3 manage.py createsuperuser
``` 
Перейти по адресу .../api/v1/jwt/create/ и отправить POST запрос с 
именем и паролем пользователя
```
{
    "username": "example_name",
    "password": "example_password"
}
``` 
Получить токен (в ключе access) и передать его в headers
```
KEY: Authorization
VALUE: Bearer <ваш токен>
``` 
## Примеры запросов
**Полный список запросов можно посмотреть перейдя на .../redoc/ 
развернутого проекта**
