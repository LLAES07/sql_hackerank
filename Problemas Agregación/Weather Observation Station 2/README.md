
**[ENG]**

Query the following two values from the STATION table:

The sum of all values in LAT_N rounded to a scale of  decimal places.
The sum of all values in LONG_W rounded to a scale of  decimal places.


**[ESP]**

Consulta los siguientes dos valores de la tabla STATION:

La suma de todos los valores en LAT_N redondeada a lugares decimales.
La suma de todos los valores en LONG_W redondeada a lugares decimales.

![alt text](image.png)

**SOLUCIÓN**

```sql
SELECT
    ROUND(SUM(lat_n), 2),
    ROUND(SUM(long_w), 2)
FROM 
    station;

```


**output:**


````

42850.04 47381.48


```