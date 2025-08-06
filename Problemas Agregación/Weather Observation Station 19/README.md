



**[ENG]**
Consider $P_{1}(a, b)$  and $P_{2}(b, d)$  to be two points on a 2D plane where $(a, b)$ are the respective minimum and maximum values of Northern Latitude (LAT_N) $(c, d)$ and  are the respective minimum and maximum values of Western Longitude (LONG_W) in STATION.

Query the Euclidean Distance between points $P_{1}$ and $P_{2}$ and format your answer to display  decimal digits.

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