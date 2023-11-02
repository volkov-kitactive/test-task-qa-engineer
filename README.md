# Тестовое задание на позицию тестировщика

## Описание

В разработке находится приложение для хранения файлов, которое имеет следующий функционал: 

- Регистрация;
- Авторизация;
- Личный кабинет пользователя, где можно загружать, отображать (если добавили картинку, то отображать ее привьюшку, если документ, то иконку документа, при клике на файл скачивать его) и удалять файлы. Также в личном кабинете есть счетчик загруженных файлов и возможность выхода из личного кабинета. Всего файлов, которые пользователь может загрузить - 20, максимальный размер загружаемых данных за 1 запрос - 1MБ).

Backend разработчики подготовили API для тестирования,

- POST - /api/register - Регистрация пользователя, принимает email, password, name;
- POST - /api/login - Получение токена доступа, принимает email, password;
- POST - /api/logout - Выход. Требует токен доступа;
- GET - /api/media - Получение файлов. Требует токен доступа. Выгружает массив файлов (files), каждый объект содержит: id, name, fileName, mimeType, url, createdAt;
- POST - /api/media/upload - Загрузка файлов. Требует токен доступа. Принимает массив файлов files;
- GET - /api/media/{id} - Получение файла. Требует токен доступа.
- DELETE - /api/media/{id} - Удаление файла. Требует токен доступа.

Токен передается в заголовке Authorization, со значением Bearer {token}

## Требуется

- продумать и составить план тестирования с подробным описанием кейсов;
- в Postman создать fake запросы для API и экспортировать;
- описать как бы вы проводили нагрузочное тестирование и тестирование безопасности данного сервиса.
