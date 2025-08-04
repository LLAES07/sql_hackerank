
**[ENG]**
Query the sum of Northern Latitudes (LAT_N) from STATION having values greater than 38.7880  and less than 137.2345 . Truncate your answer to  decimal places.

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