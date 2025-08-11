



**[ENG]**
Consider $P_{1}(a, b)$  and $P_{2}(b, d)$  to be two points on a 2D plane where $(a, b)$ are the respective minimum and maximum values of Northern Latitude (LAT_N) $(c, d)$ and  are the respective minimum and maximum values of Western Longitude (LONG_W) in STATION.

Query the Euclidean Distance between points $P_{1}$ and $P_{2}$ and format your answer to display  decimal digits.


**[ESP]**  
Considera que $P_{1}(a, b)$ y $P_{2}(c, d)$ son dos puntos en un plano 2D, donde $(a, b)$ son respectivamente los valores mínimo y máximo de Latitud Norte (LAT_N), y $(c, d)$ son respectivamente los valores mínimo y máximo de Longitud Oeste (LONG_W) en STATION.

Consulta la Distancia Euclidiana entre los puntos $P_{1}$ y $P_{2}$ y da formato a tu respuesta para que muestre una cierta cantidad de cifras decimales.


![alt text](image.jpg)

**SOLUCIÓN**

```sql


SELECT
    TRUNCATE(SQRT(POWER((MAX(lat_n) - MIN(lat_n)), 2) + POWER((MAX(long_w) - MIN(long_w)), 2)), 4)
FROM
    station

```


**output:**


````

184.1616


```