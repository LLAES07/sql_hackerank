
**[ENG]**
Consider $P_{1}(a, b)$  and $P_{2}(c, d)$ to be two points on a 2D plane.

 a happens to equal the minimum value in Northern Latitude (LAT_N in STATION).
 b happens to equal the minimum value in Western Longitude (LONG_W in STATION).
 c happens to equal the maximum value in Northern Latitude (LAT_N in STATION).
 d happens to equal the maximum value in Western Longitude (LONG_W in STATION).
Query the Manhattan Distance between points $P_{1}$ and $P_{2}$ and round it to a scale of  decimal places.

**[ESP]**  
Considera que $P_{1}(a, b)$ y $P_{2}(c, d)$ son dos puntos en un plano 2D.

$a$ corresponde al valor mínimo de Latitud Norte (LAT_N en STATION).  
$b$ corresponde al valor mínimo de Longitud Oeste (LONG_W en STATION).  
$c$ corresponde al valor máximo de Latitud Norte (LAT_N en STATION).  
$d$ corresponde al valor máximo de Longitud Oeste (LONG_W en STATION).  
Consulta la Distancia Manhattan entre los puntos $P_{1}$ y $P_{2}$ y redondéala a una cierta cantidad de cifras decimales.

![alt text](image.jpg)

**SOLUCIÓN**

```sql
SELECT 
    ROUND((MAX(lat_n) - MIN(lat_n)) + (MAX(long_w) - MIN(long_w)), 4) AS manhattan_distance
FROM 
    station;


```


**output:**


````
259.6859


```