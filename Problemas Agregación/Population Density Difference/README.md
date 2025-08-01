
**[ENG]**
Query the difference between the maximum and minimum populations in CITY.





![alt text](image.jpg)


**SOLUCIÓN**

```sql
SELECT
    (SELECT 
        MAX(population)
    FROM
        city ) -
    (SELECT
        MIN(population)
    FROM
        city) AS diferencia_total


```


**output:**


````

4695354



```