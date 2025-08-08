
**[ENG]**
Query the sum of Northern Latitudes (LAT_N) from STATION having values greater than 38.7880  and less than 137.2345 . Truncate your answer to  decimal places.

**[ESP]**

Consulta la suma de las latitudes del norte (LAT_N) de la tabla STATION que tengan valores mayores que 38.7880 y menores que 137.2345. Trunca tu respuesta a lugares decimales.
![alt text](image.png)

**SOLUCIÓN**

```sql
SELECT 
    TRUNCATE(SUM(lat_n), 4)
FROM 
    station
WHERE 
    lat_n > 38.7880 
    AND lat_n < 137.2345;

```


**output:**


````
36354.8135


```