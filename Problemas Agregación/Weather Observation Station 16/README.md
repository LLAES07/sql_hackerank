
**[ENG]**
Query the smallest Northern Latitude (LAT_N) from STATION that is greater than 38.7780 . Round your answer to 4 decimal places.

**[ESP]**

Consulta la latitud norte (LAT_N) más pequeña de STATION que sea mayor que 38.7780. Redondea tu respuesta a 4 lugares decimales.

![alt text](image.jpg)

**SOLUCIÓN**

```sql




SELECT
    ROUND(MIN(lat_n), 4) AS minimo
FROM
    station
WHERE
    lat_n > 38.7780

```


**output:**


````
38.8526



```