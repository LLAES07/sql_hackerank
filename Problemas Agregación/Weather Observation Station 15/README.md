
**[ENG]**

Query the Western Longitude (LONG_W) for the largest Northern Latitude (LAT_N) in STATION that is less than 137.2345. Round your answer to  decimal places.

**[ESP]**

Consulta la longitud occidental (LONG_W) correspondiente a la mayor latitud norte (LAT_N) en STATION que sea menor que 137.2345. Redondea tu respuesta a lugares decimales.

![alt text](image.jpg)

**SOLUCIÓN**

```sql
SELECT 
    ROUND(LONG_W, 4)
FROM 
    STATION
WHERE 
    LAT_N = (
        SELECT 
            MAX(LAT_N)
        FROM 
            STATION
        WHERE 
            LAT_N < 137.2345
    );



```


**output:**


````
117.2465



```