
**[ENG]**
Consider $P_{1}(a, b)$  and $P_{2}(c, d)$ to be two points on a 2D plane.

 happens to equal the minimum value in Northern Latitude (LAT_N in STATION).
 happens to equal the minimum value in Western Longitude (LONG_W in STATION).
 happens to equal the maximum value in Northern Latitude (LAT_N in STATION).
 happens to equal the maximum value in Western Longitude (LONG_W in STATION).
Query the Manhattan Distance between points $P_{1}$ and $P_{2}$ and round it to a scale of  decimal places.

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