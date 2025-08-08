
**[ENG]**

Query the total population of all cities in CITY where District is California.

**[ESP]**

Consulta la población total de todas las ciudades en CITY donde el Distrito sea California.

![alt text](image.jpg)


**SOLUCIÓN**

```sql

SELECT
    SUM(population) AS poblacion_total

FROM
    city

WHERE
    lower(DISTRICT) LIKE 'california';



```


**output:**


````

339002


```