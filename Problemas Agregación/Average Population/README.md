
**[ENG]**

Query the average population for all cities in CITY, rounded down to the nearest integer.



![alt text](image.jpg)


**SOLUCIÓN**

```sql
SELECT 
    FLOOR(AVG(population)) AS average_population
FROM 
    city;


```


**output:**


````

454250



```