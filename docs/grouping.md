# Группировка

## GROUP BY

```
SELECT value, SUM(value2)
FROM table
GROUP BY value;
```

### Группировка по выражениям

```
SELECT SUBSTR(date, 1, 7) AS month,
    SUM(amount)
FROM sales
GROUP BY month;
```

### HAVING

используется для фильтрации данных после группировки

```
SELECT value, COUNT(*) AS value1 FROM table
GROUP BY value HAVING COUNT(*) > 10;
```

