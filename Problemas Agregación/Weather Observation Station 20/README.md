
**[ENG]**
A median is defined as a number separating the higher half of a data set from the lower half. Query the median of the Northern Latitudes (LAT_N) from STATION and round your answer to 4 decimal places.

![alt text](image.jpg)

**SOLUCIÓN**

```sql

SELECT
    ROUND(AVG(lat_n), 4) AS median_lat_n
FROM (
    SELECT
        lat_n,
        ROW_NUMBER() OVER (ORDER BY lat_n) AS row_asc,
        ROW_NUMBER() OVER (ORDER BY lat_n DESC) AS row_desc,
        COUNT(*) OVER () AS total_count
    FROM station
) t
WHERE row_asc IN (FLOOR((total_count + 1) / 2), CEIL((total_count + 1) / 2));


```


**output:**


````

83.8913

```