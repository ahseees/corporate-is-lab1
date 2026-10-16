# Corporate IS - Lab 1

Учебный проект: Django + PostgreSQL (Docker Compose).

## Как запустить

1. Установить Git, Docker Desktop, Python 3 и Node.js.
2. Клонировать репозиторий и перейти в его папку.
3. Создать виртуальное окружение и установить зависимости:
   python -m venv venv
   venv\Scripts\activate
   pip install -r requirements.txt
4. Скопировать .env.example в .env.
5. Запустить базу данных: docker compose up -d
6. Применить миграции и создать администратора:
   python manage.py migrate
   python manage.py createsuperuser
7. Запустить сервер: python manage.py runserver
   (если порт 8000 недоступен, указать другой, например runserver 12345)
8. Админка: http://127.0.0.1:8000/admin/

## Что сделано

- Django-проект config, подключённый к PostgreSQL через переменные окружения.
- PostgreSQL 16 запускается через docker-compose.yml.
- Приложение employees с моделью Employee (ФИО, должность, дата найма), доступное в админке.

## Идея мини-ИС для итогового проекта

Система учёта сотрудников и отпусков небольшой компании: карточки сотрудников,
отделы, заявки на отпуск и их согласование руководителем.
