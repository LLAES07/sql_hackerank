
**[ENG]**

Write a query that prints a list of employee names (i.e.: the name attribute) from the Employee table in alphabetical order.

![alt text](image.png)


**SOLUCIÓN**

```sql
SELECT 
    (SELECT COUNT(*) FROM STATION) - (SELECT COUNT(DISTINCT CITY) FROM STATION);

```


**output:**


````
13


```