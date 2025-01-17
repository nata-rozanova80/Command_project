
# Система управления заказами (Command_project)

**Система управления заказами** — это простое приложение для отслеживания и управления заказами в бизнесе с использованием графического интерфейса на базе Tkinter и базы данных SQLite. В нем можно добавлять заказы, просматривать их список и помечать заказы как завершенные.

## Описание

Приложение позволяет:
- Добавлять новые заказы с именем клиента и деталями заказа.
- Просматривать список всех заказов.
- Завершать заказ, обновляя его статус на "Завершён".

Приложение использует SQLite для хранения данных о заказах и Tkinter для графического интерфейса.

## Функции
1. Добавление заказа
- Введите имя клиента и детали заказа в соответствующие поля.
- Нажмите кнопку "Добавить заказ" для сохранения нового заказа в базе данных.
2. Просмотр заказов
- После запуска приложения, вы увидите список всех заказов в таблице.
- Каждая строка будет содержать информацию о заказе: ID, имя клиента, детали заказа и статус.
3. Завершение заказа
- Для завершения заказа выберите заказ в таблице и нажмите кнопку "Завершить заказ".
- Статус выбранного заказа будет обновлен на "Завершён".

  
## Структура базы данных

Приложение использует SQLite для хранения данных. В базе данных есть одна таблица orders с полями:

- id: Уникальный идентификатор заказа (целое число).
- customer_name: Имя клиента (текст).
- order_details: Детали заказа (текст).
- status: Статус заказа (текст). Возможные значения: "Новый", "Завершён".


## Как это работает
При запуске приложения вызывается функция init_db(), которая создает таблицу заказов в базе данных, если она еще не существует.
Заказы добавляются в таблицу через функцию add_order(), данные берутся из полей ввода.
Функция view_orders() обновляет отображение всех заказов в таблице, запрашивая данные из базы данных.
Функция complete_order() позволяет завершить заказ, изменяя его статус на "Завершён".
