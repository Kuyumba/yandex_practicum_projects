# Проект № 4.


# Определение перспективного тарифа для телеком компании.

 Клиентам оператора сотовой связи предлагают два тарифных плана: «Смарт» и «Ультра». 

Предстоит сделать предварительный анализ тарифов на небольшой выборке клиентов.  Нужно проанализировать поведение клиентов и сделать вывод — какой тариф лучше.

## Данные

В нашем распоряжении данные 500 пользователей: кто они, откуда, каким тарифом пользуются, сколько звонков и сообщений каждый отправил за 2018 год.

Данные собраны в 5 файлов:
1. Информация о пользователях;
2. Информация о звонках;
3. Информация о сообщениях;
4. Информация об интернет-сессиях;
5. Информация о тарифах.


## Описание данных 
##### Таблица users (информация о пользователях):

|имя столбца              |описание                                                     |
|:------------------------|:------------------------------------------------------------|
| user_id | уникальный идентификатор пользователя|
| first_name | имя пользователя|
| last_name | фамилия пользователя|
| age | возраст пользователя (годы)|
| reg_date | дата подключения тарифа (день, месяц, год)|
| churn_date | дата прекращения пользования тарифом (если значение пропущено, то тариф ещё действовал на момент выгрузки данных)|
| city | город проживания пользователя|
| tariff | название тарифного плана|

##### Таблица calls (информация о звонках):

|имя столбца              |описание                                                     |
|:------------------------|:------------------------------------------------------------|
| id | уникальный номер звонка|
| call_date | дата звонка|
| duration | длительность звонка в минутах|
| user_id | идентификатор пользователя, сделавшего звонок|

##### Таблица messages (информация о сообщениях):

|имя столбца              |описание                                                     |
|:------------------------|:------------------------------------------------------------|
| id | уникальный номер сообщения|
| message_date | дата сообщения|
| user_id | идентификатор пользователя, отправившего сообщение|

##### Таблица internet (информация об интернет-сессиях):

|имя столбца              |описание                                                     |
|:------------------------|:------------------------------------------------------------|
|   id | уникальный номер сессии|
|   mb_used | объём потраченного за сессию интернет-трафика (в мегабайтах)|
|   session_date | дата интернет-сессии|
|   user_id | идентификатор пользователя|

##### Таблица tariffs (информация о тарифах):

|имя столбца              |описание                                                     |
|:------------------------|:------------------------------------------------------------|
|   tariff_name | название тарифа|
|   rub_monthly_fee | ежемесячная абонентская плата в рублях|
|   minutes_included | количество минут разговора в месяц, включённых в абонентскую плату|
|   messages_included | количество сообщений в месяц, включённых в абонентскую плату|
|   mb_per_month_included | объём интернет-трафика, включённого в абонентскую плату (в мегабайтах)|
|rub_per_minute | стоимость минуты разговора сверх тарифного пакета (например, если в тарифе 100 минут разговора в месяц, то со 101 минуты будет взиматься плата)|
|   rub_per_message | стоимость отправки сообщения сверх тарифного пакета|
|   rub_per_gb | стоимость дополнительного гигабайта интернет-трафика сверх тарифного пакета (1 гигабайт = 1024 мегабайта)|




## Задача

Наша задача — проанализировать доходы по каждому из тарифов, определить какой тариф выгоднее. 
Необходимо провести предобработку, анализ данных, ответить на следующие вопросы:
- Отличается ли средняя выручка по тарифам;
- Отличается ли средняя выручка по Москве и по всем остальным регионам.

#### Структура работы:

Часть 1. Знакомство с данными

Часть 2. Подготовка данных

    2.1. Преобразование дат к типу dtypes

    2.2. Количество сделанных звонков и израсходованных минут разговора по месяцам.

    2.3. Количество отправленных сообщений по месяцам.

    2.4. Объем израсходованного трафика по месяцам

    2.5. Сводные таблицы параметров по месяцам для каждого пользователя

    2.6. Вычисление помесячного дохода с каждого пользователя

Часть 3. Анализ данных

    3.1. Сколько минут разговора

    3.2. Сколько сообщений

    3.3. Сколько мегабайт

    3.4. Анализ выручки

Часть 4. Проверка гипотез

    4.1. Cредняя выручка пользователей тарифов «Ультра» и «Смарт»

    4.2. Средняя выручка пользователей из Москвы и из других регионов

Часть 5. Выводы

## Используемые библиотеки.
`pandas`
`numpy`
`scipy`
`math`
`matplotlib`


