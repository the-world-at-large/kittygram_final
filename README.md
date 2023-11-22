# Проект Kittygram

![GitHub Workflow Status](https://img.shields.io/github/workflow/status/the-world-at-large/kittygram_final/CI-CD)

## Описание проекта

Проект Kittygram - это веб-приложение для обмена фотографиями котиков. Пользователи могут загружать свои фотографии котиков, просматривать фотографии других пользователей, ставить лайки и оставлять комментарии.

## Автор проекта

Автор проекта: [the-world-at-large](https://github.com/the-world-at-large)

## Технологии

Проект построен с использованием следующих технологий:

- Django: фреймворк для создания веб-приложений на языке Python.
- PostgreSQL: система управления реляционными базами данных.
- Docker: контейнеризация приложения для удобного развертывания и масштабирования.
- GitHub Actions: для настройки непрерывной интеграции и доставки.

## Различия между продакшн и обычной версией

Продакшн-версия предназначена для использования в боевой среде и включает в себя дополнительные меры безопасности и оптимизации для обеспечения стабильной работы приложения. Обычная версия может использоваться для разработки и тестирования.

## Инструкция по развертыванию

### Локальное развертывание

1. Установите Docker и Docker Compose.
2. Склонируйте репозиторий: `git clone https://github.com/the-world-at-large/kittygram_final.git`.
3. Перейдите в директорию проекта: `cd kittygram`.
4. Создайте файл `.env` и укажите необходимые переменные окружения.
5. Запустите приложение: `docker-compose up`.

### Удаленное развертывание

1. Деплойте код на сервер с использованием инструментов, таких как Git.
2. Установите Docker и Docker Compose на сервере.
3. Создайте файл `.env` и укажите необходимые переменные окружения.
4. Запустите приложение: `docker-compose up`.

## Проверка работы с помощью автотестов

1. В корне репозитория создайте файл `tests.yml` с необходимыми параметрами (repo_owner, kittygram_domain, taski_domain, dockerhub_username).
2. Скопируйте содержимое файла `.github/workflows/main.yml` в файл `kittygram_workflow.yml` в корневой директории проекта.

3. Для локального запуска тестов создайте виртуальное окружение, установите зависимости из backend/requirements.txt и запустите в корневой директории проекта `pytest`.

## Чек-лист для проверки перед отправкой задания

- Проект Taski доступен по доменному имени, указанному в `tests.yml`.
- Проект Kittygram доступен по доменному имени, указанному в `tests.yml`.
- Пуш в ветку main запускает тестирование и деплой Kittygram, а после успешного деплоя вам приходит сообщение в телеграм.
- В корне проекта есть файл `kittygram_workflow.yml`.
