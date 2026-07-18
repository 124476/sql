# Выборка данных

## SELECT и FROM

используется для получения данных из таблицы

- FROM — откуда брать данные
- SELECT — какие столбцы выбрать

```
select * from products
```

## DISTINCT

оставить только уникальные строки

## ORDER BY

упорядочить результат

- asc - по возрастанию 
- desc - по убыванию

## LIMIT

ограничить количество строк

```
select * from products limit 20
```

## OFFSET

сместить количество строк (пропустить от начала)

```
select * from products offset 20
```