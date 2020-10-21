# Деплой проектов на Heroku

## Обзаведитесь сервером

Зарегистрируйтесь на [Heroku](https://id.heroku.com/login) и создайте приложение (app). 

Heroku даёт вам 550 бесплатных часов в месяц, а если привязать карту — 1000 часов.

## Опубликуйте код на GitHub

У [Heroku](https://id.heroku.com/login) есть интеграция с [GitHub](https://github.com). Не забудьте опубликовать ```requirements.txt```.

**Файл .env публиковать нельзя.**

## Подготовьте код к деплою 

Создайте [Procfile](https://devcenter.heroku.com/articles/procfile) с одной строчкой:

	bot: python3 название_файла.py

Чувствительные данные (например, токен), можно задать во вкладке Settings на сайте Heroku. Заполните Config Vars и получите их из кода такой строчкой:

	os.environ['TOKEN']

Привязать гитхаб и залить код можно на вкладке Deploy. Найдите свой репозиторий с помощью поиска и подключите его к Heroku.

По умолчанию Heroku работает только с [избранными версиями Python](https://devcenter.heroku.com/articles/python-runtimes), если Ваша версия Python отличается от указанных то необходимо создать файл ```runtime.txt``` в корневой директории приложения и указать в нем версию Python, которую используете: 

	python-3.7.4

## Установите Heroku CLI 

Консольный клиент [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli#download-and-install) удобен для просмотра логов.





