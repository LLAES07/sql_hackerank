
**[ENG]**
Query the Western Longitude (LONG_W)where the smallest Northern Latitude (LAT_N) in STATION is greater than 38.7780 . Round your answer to 4 decimal places.

**[ESP]**  
Consulta la Longitud Oeste (LONG_W) donde la Latitud Norte (LAT_N) más pequeña en STATION sea mayor que 38.7780. Redondea tu respuesta a 4 cifras decimales.

![alt text](image.jpg)

**SOLUCIÓN**

```sql

SELECT
    ROUND(long_w, 4)

FROM   
    station

WHERE
    lat_n = (SELECT 
                MIN(lat_n) 
             FROM 
                station 
             WHERE 
                lat_n > 38.7780)
```


**output:**


````
70.1378



```