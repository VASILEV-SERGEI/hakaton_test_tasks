**Цель задания:**

Приложение - мобильная утилита для сканирования документов. Модель монетизации подписочная, есть пробный период 7 дней с дальнейшим переходом в оплату 4.99 USD в неделю. По ссылке ниже выгрузка с базы данных по оформлениям подписок и оплат. Каждая строка представляет собой отдельное событие (либо оформление пробной подписки, либо оплата после завершения пробного периода). Задание построено таким образом, чтобы проверить понимание принципов unit-экономики предприятия. Задание 1 предпочтительней делать с помощью Python.

**Задание:**

Необходимо рассчитать текущий LTV юзера, используя когортный анализ (cohorting event - оформление пробного периода, когорта представляет собой кол-во возможных операций).
Спрогнозировать, каким будет LTV на полгода.
Построить график, который будет отображать кривую фактического LTV на фоне кривой прогнозируемого LTV.
Рассчитать ROMI на 4 недели и на полгода, если стоимость привлечения платящего пользователя 6 USD (ROMI нужно брать операционный, а не бухгалтерский, цель: узнать как окупятся наши инвестиции).


**Описание данных:**

В ТЗ описание данных не предоставленно. Будем учитывать наименование столбца и составим описание данных самостоятельно.

product_id: наименование продукта
quantity: количество
is_trial_period: пробный период
purchase_date: дата покупки
user_id: идентификатор пользователя

**Общий вывод:**

В результате работы с данными были получены следующие результаты:

1) Выполнена предобработка данных, а именно:

- Датасет проверен на соответствие форматов данных;
- Датасет проверен на пропуски. Пропущенных значений не обнаружено;
- Датасет проверен на дубликаты, выявлено 84 явных дубликата. Дубликаты были удалены, процент потерь составил 0.07%.
  
2) Произведен расчёт LTV пользователей приложения используя когортный анализ, прирост LTV также отображен на линейном графике;
3) Произведен прогнозный расчёт LTV на полгода(до августа 2020) с использованием среднего значения LTV на основе исторических данных;
4) Построен график на котором отображен текущий LTV и прогнозный LTV;
5) Расчитан ROMI (Return on Marketing Investment) на 4 недели и полгода.