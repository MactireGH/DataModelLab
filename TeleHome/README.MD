# Проект Телекоммуникации

Оператор связи «ТелеДом» хочет бороться с оттоком клиентов. Для этого его сотрудники начнут предлагать промокоды и специальные условия всем, кто планирует отказаться от услуг связи. Чтобы заранее находить таких пользователей, «ТелеДому» нужна модель, которая будет предсказывать, разорвёт ли абонент договор. Команда оператора собрала персональные данные о некоторых клиентах, информацию об их тарифах и услугах. Ваша задача — обучить на этих данных модель для прогноза оттока клиентов.

## Описание услуг

Оператор предоставляет два основных типа услуг:

- Стационарную телефонную связь. Телефон можно подключить к нескольким линиям одновременно.
- Интернет. Подключение может быть двух типов: через телефонную линию (`DSL`, от англ. digital subscriber line — «цифровая абонентская линия») или оптоволоконный кабель (`Fiber optic`).

Также доступны такие услуги:

- Антивирус `DeviceProtection`
- Блокировка небезопасных сайтов `OnlineSecurity`
- Выделенная линия технической поддержки `TechSupport`
- Облачное хранилище файлов `OnlineBackup`
- Стриминговое телевидение `StreamingTV`
- Каталог фильмов `StreamingMovies`

Клиенты могут платить за услуги каждый месяц или заключить договор на 1–2 года. Возможно оплатить счёт разными способами, а также получить электронный чек.

## Описание данных

Данные состоят из нескольких файлов, полученных из разных источников:

- `contract_new.csv` - информация о договоре
- `personal_new.csv` - персональные данные клиента
- `internet_new.csv` - информация об интернет-услугах
- `phone_new.csv`- информация об услугах телефонии

Файл `contract_new.csv`

- `customerID` - идентификатор абонента
- `BeginDate` - дата начала действия договора
- `EndDate` - дата окончания действия договора
- `Type` - тип оплаты: раз в год-два или ежемесячно
- `PaperlessBilling` - электронный расчётный лист
- `PaymentMethod` - тип платежа
- `MonthlyCharges` - расходы за месяц
- `TotalCharges` - общие расходы абонента

Файл `personal_new.csv`

- `customerID` - идентификатор пользователя
- `gender` - пол
- `SeniorCitizen` - является ли абонент пенсионером
- `Partner` - есть ли у абонента супруг или супруга
- `Dependents` - есть ли у абонента дети

Файл `internet_new.csv`

- `customerID` - идентификатор пользователя
- `InternetService` - тип подключения
- `OnlineSecurity` - блокировка опасных сайтов
- `OnlineBackup` - облачное хранилище файлов для резервного копирования данных
- `DeviceProtection` - антивирус
- `TechSupport` - выделенная линия технической поддержки
- `StreamingTV` - стриминговое телевидение
- `StreamingMovies` - каталог фильмов

Файл `phone_new.csv`

- `customerID` - идентификатор пользователя
- `MultipleLines` - подключение телефона к нескольким линиям одновременно

Во всех файлах столбец `customerID` содержит код клиента. Информация о договорах актуальна на 1 февраля 2020 года.

## План работы

1. Анализ и просмотр исходных данных.
2. Предобработка данных (Очистка, добавление признаков).
3. Исследовательский анализ.
4. Корреляционный анализ.
5. Построение модели машинного обучения.
6. Оценка важности признаков.
7. Оценка качество предсказаний.
8. Вывод

## Цель проекта

Построить модель машинного обучения, прогнозирующая уход клиента.