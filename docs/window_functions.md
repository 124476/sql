# Оконные функции

## OVER

Оконная функция — это функция, которая выполняется по набору строк,
но возвращает результат для каждой строки отдельно

```
SELECT id, value,
    AVG(value) OVER () AS avg_value
FROM table;
```

## PARTITION BY

Позволяет разбить данные на группы, без потери данных

```
SELECT id, user_id, value,
    AVG(value) OVER (PARTITION BY user_id) AS avg_per_user
FROM table;
```

## ORDER BY и ранжирование

ORDER BY внутри OVER(...) задаёт порядок строк для вычисления оконной функции

```
SELECT
    value_date,
    value,
    ROW_NUMBER() OVER (ORDER BY value DESC) AS rank_by_value
FROM table;
```
