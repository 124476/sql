# Подзапросы

SELECT запросы можно делать внутри другогих SELECT запросов

```
SELECT id, value,
    (SELECT MAX(value) FROM table) AS max_value
FROM sales;
```

## WITH

позволяет разделить запрос на шаги

```
WITH avg_values AS (
    SELECT AVG(value) AS avg_value
    FROM table
)
SELECT
    id,
    value
FROM table
WHERE value > (
    SELECT avg_value
    FROM avg_values
);
```

