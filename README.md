# Описание проекта:
В проекте представлена работа с базой данных и автоматизация 
теста ЯндексСамоката. Яндекс Самокат - это сервис, который позволяет арендовать электрический самокат на несколько дней.

- Язык приложения — `JavaScript`.
- Среда - `Node.js v12.17.0`
- Доступ к приложению по протоколу `HTTP 1.1`.
- Документация к приложению осуществляется с помощью модуля `apiDoc`.
- Приложение использует базу данных — `PostgreSQL`.

### Требования

- Для запуска тестов должны быть установлены пакеты `pytest` и `requests`.
- Запуск всех тестов выполняется командой `pytest`.

## 1. Работа с базой данных
Запросы расположены в файле `SQL.md`, результаты выполнения запросов расположены 
в файлах `sql_query_1.png` и `sql_query_2.png`

### Задание 1
Нужно проверить, отображается ли созданный заказ в базе данных.
Для этого необходимо вывести список логинов курьеров с количеством их заказов в статусе «В доставке» (поле inDelivery = true). 

### Задание 2

Надо протестировать статусы заказов. Нужно убедиться, что в базе данных они записываются корректно.
Для этого необходимо вывести все трекеры заказов и их статусы. 
Статусы определяются по следующему правилу:
Если поле finished == true, то вывести статус 2.
Если поле canсelled == true, то вывести статус -1.
Если поле inDelivery == true, то вывести статус 1.
Для остальных случаев вывести 0.

## 2. Автоматизация теста.
Автотест расположен в файле `sender_stand_request.py`, результаты выполнения автотеста расположены 
в файле `autotest_results.png`
### Задание
Необходимо автоматизировать сценарий, который подготовили тестировщики:
1. Клиент создает заказ.  
2. Проверяется, что по треку заказа можно получить данные о заказе.

### Шаги выполнения автотеста

1. Для запуска теста необходимо в файл configuration.py вставить актуальный URL стенда (пример: 
https://68b0eca5-2eab-424b-aa7a-b56d7c658e73.serverhub.praktikum-services.ru)
2. В файле sender_stand_request.py нажать кнопку Run или ввести в терминале команду `pytest`

## Стек для выполнения проекта
* PyCharm
* GitHub
* requests
* pytest