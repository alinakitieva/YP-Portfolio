# Классификация клиентов телеком компании

## Статус проекта
Завершен

## Задачи проекта
На основе данных предложить клиенту тариф.

## Описание проекта
Оператор мобильной связи выяснил: многие клиенты пользуются архивными тарифами. Они хотят построить систему, 
способную проанализировать поведение клиентов и предложить пользователям один из новых тариф.

## Ключевые слова
классификация, подбор гиперпараметров, выбор модели МО

## Описание данных
Каждый объект в наборе данных — это информация о поведении одного пользователя за месяц.
- сalls — количество звонков,
- minutes — суммарная длительность звонков в минутах,
- messages — количество sms-сообщений,
- mb_used — израсходованный интернет-трафик в Мб,
- is_ultra — каким тарифом пользовался в течение месяца («Ультра» — 1, «Смарт» — 0).

## Вывод
В ходе выполнения данного проекта, мы прошли следующие этапы:

1. Загрузили и изучили данные, содержащие информацию о поведении клиентов оператора мобильной связи «Мегалайн».
2. Разделили данные на обучающую, валидационную и тестовую выборки.
3. Исследовали различные модели классификации с разными гиперпараметрами, включая случайный лес (Random Forest), логистическую регрессию (Logistic Regression) и дерево решений (Decision Tree Classifier).
4. Выбрали наилучшую модель (Random Forest) на основе точности на валидационной выборке.
5. Протестировали выбранную модель на тестовой выборке и оценили её точность - 81%.
6. Проверили адекватность выбранной модели путем сравнения с базовым классификатором.

В результате анализа была выбрана модель с наилучшей точностью на валидационной выборке - Random Forest. Точность этой модели на тестовой выборке удовлетворяет критерию успешности проекта (точность больше или равна 0.75) и составляет 81%. Кроме того, модель показала адекватность, так как её точность выше, чем у базового классификатора.