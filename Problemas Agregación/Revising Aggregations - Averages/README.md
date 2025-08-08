
**[ENG]**

Query the average population of all cities in CITY where District is California.

**[ESP]**

Consulta la población promedio de todas las ciudades en CITY donde el Distrito sea California.

![alt text](image.jpg)


**SOLUCIÓN**

```sql
SELECT
    AVG(population) AS avg_poblacion

FROM
    city

WHERE
    lower(DISTRICT) LIKE 'california';


```


**output:**


````
113000.667



```