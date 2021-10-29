# Проект Yamdb

Проект YaMDb собирает отзывы (Review) пользователей на произведения (Titles). Произведения делятся на категории: «Книги», «Фильмы», «Музыка». Сами произведения в YaMDb не хранятся.

Посмотреть отзывы могут любые пользователи. Для написания собственных отзывов, комментирования и оценки необходима регистрация


## Используемые технологии

- Python
- Django
- Django Rest Framework
- PostgreSQL
- Docker

## Запуск приложения
Запустите терминал

Клонируйте репозиторий 
```
git clone https://github.com/Palashnenkoff/infra_sp2.git
```
Если Docker еще не устанвлен скачайте и установите его по ссылке https://www.docker.com/products/docker-desktop

Перейдите в директорию с проектом
```
cd infra_sp2
```

#### **Так как переменные базы данных подгружаются из скрытого файла .env,  переименуйте файл .env.example в .env и внем же установите свой пароль для доступа к БД**

Для запуска проекта выполните команду из корневой директории проекта

```
docker-compose up -d
```

Будет проведена сборка образа по Dockerfile и запуск проекта в трех контейнерах

Зайдите в контейнер web и примените миграции:
```
docker-compose exec web python manage.py migrate
```

Теперь проект доступен по адресу http://127.0.0.1/admin/
Описание API проекта доступно по адресу http://127.0.0.1/redoc/


## Создание суперпользователя

Для создания суперпользователя выполните в терминале команду 
```
docker-compose exec web python manage.py createsuperuser
```
Выполняется вход в контейнер web, где manage.py создает суперпользователя. 
Ввдите логин, почту и пароль

## Заполнение базы начальными данными

Начальные данные хранятся в файле fixtures.json.
Для заполнения базы этими данными выполните команду:

```
docker-compose exec web python manage.py loaddata fixtures.json
```
В админке http://127.0.0.1/admin/ в разделах Categories	Genres и Titles появятся тестовые данные. 
***

# Реккомендации при сворачивании проекта(очистка памяти):
* Остановка и удаление контейнеров:
```
docker-compose down
```
* Удаление образов (!команда удалит все неиспользуемые образы! если есть нужные образы лучше удалять по id):
```
docker system prune -a
```
* Удаление **всех** неиспользуемых томов:
```
docker volume prune
```
