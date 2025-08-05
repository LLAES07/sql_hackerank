
**[ENG]**
Query the greatest value of the Northern Latitudes (LAT_N) from STATION that is less than 137.2345 . Truncate your answer to  decimal places.

![alt text](image.jpg)

**SOLUCIÓN**

```sql

SELECT
    TRUNCATE(MAX(lat_n), 4)
FROM
    station
WHERE
    lat_n < 137.2345;

```


**output:**


````
137.0193



```