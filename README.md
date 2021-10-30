# **Проект YamDB**

YamDB - это база отзывов о фильмах, книгах и музыке. Здесь пользователь может оставить отзыв (Review) и выставить рейтинг произведению (Title). Произведения делятся на категории: «Книги», «Фильмы», «Музыка». При этом список категорий (Category) может быть расширен. Сами произведения в YamDB не хранятся.

Посмотреть отзывы могут любые пользователи. Для написания собственных отзывов, комментирования и оценки необходима регистрация

## **Оглавление**
* [Используемые технологии](https://github.com/Palashnenkoff/infra_sp2/blob/master/README.md#%D0%B7%D0%B0%D0%BF%D1%83%D1%81%D0%BA-%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F)
* [Запуск приложения](https://github.com/Palashnenkoff/infra_sp2/blob/master/README.md#%D0%B7%D0%B0%D0%BF%D1%83%D1%81%D0%BA-%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F)
* [Запуск приложения с помощь контейнеризации Docker](https://github.com/Palashnenkoff/infra_sp2/blob/master/README.md#%D0%B7%D0%B0%D0%BF%D1%83%D1%81%D0%BA-%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F-%D1%81-%D0%BF%D0%BE%D0%BC%D0%BE%D1%89%D1%8C-%D0%BA%D0%BE%D0%BD%D1%82%D0%B5%D0%B9%D0%BD%D0%B5%D1%80%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D0%B8-docker)
  * [Создание суперпользователя](https://github.com/Palashnenkoff/infra_sp2/blob/master/README.md#%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-%D1%81%D1%83%D0%BF%D0%B5%D1%80%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8F)
  * [Заполнение базы начальными данными](https://github.com/Palashnenkoff/infra_sp2/blob/master/README.md#%D0%B7%D0%B0%D0%BF%D0%BE%D0%BB%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B1%D0%B0%D0%B7%D1%8B-%D0%BD%D0%B0%D1%87%D0%B0%D0%BB%D1%8C%D0%BD%D1%8B%D0%BC%D0%B8-%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D0%BC%D0%B8)
  * [Реккомендации при сворачивании проекта (очистка памяти)](https://github.com/Palashnenkoff/infra_sp2/blob/master/README.md#%D1%80%D0%B5%D0%BA%D0%BA%D0%BE%D0%BC%D0%B5%D0%BD%D0%B4%D0%B0%D1%86%D0%B8%D0%B8-%D0%BF%D1%80%D0%B8-%D1%81%D0%B2%D0%BE%D1%80%D0%B0%D1%87%D0%B8%D0%B2%D0%B0%D0%BD%D0%B8%D0%B8-%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B0%D0%BE%D1%87%D0%B8%D1%81%D1%82%D0%BA%D0%B0-%D0%BF%D0%B0%D0%BC%D1%8F%D1%82%D0%B8)
* [Локальный запуск приложения](https://github.com/Palashnenkoff/infra_sp2/blob/master/README.md#%D0%BB%D0%BE%D0%BA%D0%B0%D0%BB%D1%8C%D0%BD%D1%8B%D0%B9-%D0%B7%D0%B0%D0%BF%D1%83%D1%81%D0%BA-%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F)
  * [Создание суперпользователя](https://github.com/Palashnenkoff/infra_sp2/blob/master/README.md#%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-%D1%81%D1%83%D0%BF%D0%B5%D1%80%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8F-1)
  * [Заполнение базы начальными данными](https://github.com/Palashnenkoff/infra_sp2/blob/master/README.md#%D0%B7%D0%B0%D0%BF%D0%BE%D0%BB%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B1%D0%B0%D0%B7%D1%8B-%D0%BD%D0%B0%D1%87%D0%B0%D0%BB%D1%8C%D0%BD%D1%8B%D0%BC%D0%B8-%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D0%BC%D0%B8-1)



## **Используемые технологии**

![](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=green)
![](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![](https://img.shields.io/badge/DJANGO-REST-ff1709?style=for-the-badge&logo=django&logoColor=white&color=ff1709&labelColor=gray)
![](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=JSON%20web%20tokens&logoColor=white)
![](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)

## ***Запуск приложения***
Приложение можно запустить двумя способами. С помошью контейнеров Docker или локально на сервере Django. Ниже представлены интсрукции по запуску

Запустите терминал и клонируйте репозиторий 
```
git clone https://github.com/Palashnenkoff/YamDB.git
```
Перейдите в директорию с проектом
```
cd YamDB
```

## **Запуск приложения с помощь контейнеризации Docker** 
Если Docker еще не устанвлен скачайте и установите его по ссылке https://www.docker.com/products/docker-desktop

Так как переменные базы данных подгружаются из скрытого файла .env,  переименуйте файл .env.example в .env и внем же установите свой пароль для доступа к БД. Переменные для локального запуска удалите или закомментируйте.
```
.env.example -> .env
```

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
Вам может пригодиться супер-пользователь - он позволяет быстро и удобно создавать пользователей, посты, комментарии и другие сущности.
Для создания суперпользователя выполните в терминале команду 
```
docker-compose exec web python manage.py createsuperuser
```
Выполняется вход в контейнер web, где manage.py создает суперпользователя. 
Ввдите логин, почту и пароль

После успешного создания суперпользователя и ввода логин/пароль на страницу http://127.0.0.1/admin/ открывается доступ к интерфейсу администратора (админ-панель).

## Заполнение базы начальными данными

Начальные данные хранятся в файле fixtures.json.
Для заполнения базы этими данными выполните команду:

```
docker-compose exec web python manage.py loaddata fixtures.json
```
В админке http://127.0.0.1/admin/ в разделах Categories	Genres и Titles появятся тестовые данные. 

## *Реккомендации при сворачивании проекта (очистка памяти)*
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

## Локальный запуск приложения

Из директории приложения (YamDB) создайте и активируйте виртуальное окружение:
###### * для Mac или Linux 'python3 -m venv venv'  
```
python -m venv venv
```
###### * для Mac или Linux 'source venv/bin/activate' 
```
source venv/Scripts/activate 
```
Обновите pip и установите зависимости:
```
python -m pip install --upgrade pip

pip install -r requirements.txt
```
Так как переменные базы данных подгружаются из скрытого файла .env,  переименуйте файл .env.example в .env и внем же установите свой пароль для доступа к БД и название БД (**БД PostgreSQL с таким названием должна быть заранее создана, например с помощю pgAdmin (database GUI)**). Переменные для запуска через Docker удалите или закомментируйте.
```
.env.example -> .env
```

Выполните миграции:
```
python manage.py migrate
```
## Создание суперпользователя
Для создания суперпользователя выполните команду:
```
python manage.py createsuperuser
```
## Заполнение базы начальными данными
Начальные данные хранятся в файле fixtures.json.
Для заполнения базы этими данными выполните команду:

```
python manage.py loaddata fixtures.json
```

Запустите проект:
```
python manage.py runserver
```

Теперь проект доступен по адресу http://127.0.0.1/admin/
Описание API проекта доступно по адресу http://127.0.0.1/redoc/
