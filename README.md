# Проведение аналитики покупок в e-commerce с помощью когортного и RFM-анализа

**Статус проекта:** Закончен.

**Описание проекта:**
Проведен EDA, проанализировано поведение клиентов, статусы заказов и частота их покупок по неделям. 
Проведен когортный анализ пользователей. Была проведена RFM-сегментация пользователей для исследования аудитории.

**Задачи проекта:**
1. Сколько у нас пользователей, которые совершили покупку только один раз? 
2. Сколько заказов в месяц в среднем не доставляется по разным причинам (вывести детализацию по причинам)?
3. По каждому товару определить, в какой день недели товар чаще всего покупается.
4. Сколько у каждого из пользователей в среднем покупок в неделю (по месяцам)?
5. Проведи когортный анализ пользователей. В период с января по декабрь выяви когорту с самым высоким retention на 3й месяц.
6. построй RFM-сегментацию пользователей, чтобы качественно оценить свою аудиторию. В кластеризации можешь выбрать следующие метрики: 
  R - время от последней покупки пользователя до текущей даты, F - суммарное количество покупок у пользователя за всё время, 
  M - сумма покупок за всё время. Подробно опиши, как ты создавал кластеры. Для каждого RFM-сегмента построй границы метрик recency, frequency и monetary 
  для интерпретации этих кластеров.

**Навыки и инструменты:** `Python`; `Pandas`; `Matplotlib`; `NumPy`; `Seaborn`; `Plotly`.

**Общий вывод:** >95% всех покупателей совершили покупку только один раз, может говорить о том, что продукт, который реализует компания, имеет долгий срок потребления 
(~1 покупка за один-два года). К тому же, нам неизвестно, в чем измеряется цена товара, поэтому можно предположить, что данные собраны о продажах 
крупной техники/электроники или автомобилей (например, у неофициального диллера).

Таким образом, кажется логичным следующее разделение клиентов на сегменты:

VIP-клиенты - покупали относительно часто, на большую сумму и последняя покупка была недавно (R-score 3-4; F-score 3-4; M-score 3-4)
Нельзя потерять - покупали часто на большую сумму, но давно (R-score 1-2; F-score 3-4; M-score 3-4)
Требующие внимания - покупали редко на большую сумму, но давно (R-score 1-2; F-score 1-2; M-score 3-4)
Лояльные - купили дважды, в последний раз - недавно и на большую сумму (R-score 3-4; F-score 2; M-score 3-4)
Потенциально лояльные - купили однажды недавно и на большую сумму (R-score 3-4; F-score 1; M-score 3-4)
Подающие надежды - покупали 2-3 раза, последний раз недавно, но на маленькие суммы (R-score 3-4; F-score 2-3; M-score 1-2)
Недавние - купили недавно и на маленькую сумму (R-score 3-4; F-score 1; M-score 1-2)
Почти уснувшие - покупали часто, но давно и на маленькие суммы (R-score 1-2; F-score 2-4; M-score 1-2)
Потерянные - купили однажды давно и на маленькую сумму (R-score 1-2; F-score 1; M-score 1-2)
