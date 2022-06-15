YamDB
=====
---
### Описание:
Проект YaMDb собирает отзывы пользователей на различные произведения.

### Технологии:
Проект реализован на django + python с использованием djangorestframework

### Инструкции по запуску:

#### Описание env-файла

* DB_ENGINE - _Тип БД_
* DB_NAME - _Имя БД_
* POSTGRES_USER - _Имя пользователя БД_
* POSTGRES_PASSWORD - _Пароль_
* DB_HOST _Адрес БД_
* DB_PORT _Порт_

* SECRET_KEY _Секретный ключ_ 
* ADMIN_EMAIL _Почта администратора_


Запуск с Docker:

```
cd infra
docker-compose up -d
```

После запуска всех контейнеров

```
docker-compose exec python manage.py migrate
docker-compose exec python manage.py createsuperuser
docker-compose exec python manage.py collectstatic
```

Описание и примеры запросов к API:

[http://127.0.0.1/redoc](http://127.0.0.1/redoc)

Админ панель:

[http://127.0.0.1/admin](http://127.0.0.1/admin)

Остановить контейнеры:

```docker-compose down```



### Автор:
Алексей Лагунов 

[sapp1507@gmail.com](sapp1507@gmail.com) 