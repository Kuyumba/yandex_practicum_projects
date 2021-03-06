### Проект № 6.

# Построение модели для подбора подходящего тарифа мобильной связи.

Оператор мобильной связи выяснил: многие клиенты пользуются архивными тарифами. Заказчик хочет построить систему, способную проанализировать поведение клиентов и предложить пользователям новый тариф: «Смарт» или «Ультра».

В нашем распоряжении данные о поведении клиентов, которые уже перешли на эти тарифы . Нужно построить модель для задачи классификации, которая выберет подходящий тариф. Предобработка данных не понадобится.

Необходимо построить модель с максимально большим значением accuracy. Нужно довести долю правильных ответов по крайней мере до 0.75. 


## Описание данных

Каждый объект в наборе данных — это информация о поведении одного пользователя за месяц. 
Известно:

|имя столбца              |описание                                                     |
|:------------------------|:------------------------------------------------------------|
| <b>сalls</b> | — количество звонков|
| <b>minutes</b> | — суммарная длительность звонков в минутах|
| <b>messages</b> | — количество sms-сообщений|
| <b>mb_used</b> | — израсходованный интернет-трафик в Мб|
| <b>is_ultra</b> | — каким тарифом пользовался в течение месяца («Ультра» — 1, «Смарт» — 0)|



## Задача

Наша задача — построить модель логистической регрессии.

    План работы
    Шаг 1. Подключение библиотек. Знакомство с данными.
    Шаг 2. Разбить данные на три выборки: обучающую (60%), валидационную(20%) и тестовую(20%)
    Шаг 3. Исследовать качество различных моделей, меняя гиперпараметры (логистическая регрессия, решающее дерево и случайный лес)
    Шаг 4. Выбрать лучшую модель и проверить её на тестовой выборке
    Шаг 5. Проверить модели на адекватность


## Используемые библиотеки.
`pandas`
`sklearn`

