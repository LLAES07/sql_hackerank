
**[ENG]**

Find the difference between the total number of CITY entries in the table and the number of distinct CITY entries in the table.
The STATION table is described as follows:

where LAT_N is the northern latitude and LONG_W is the western longitude.

For example, if there are three records in the table with CITY values 'New York', 'New York', 'Bengalaru', there are 2 different city names: 'New York' and 'Bengalaru'.

![alt text](image.png)


**SOLUCIÓN**

```sql
SELECT 
    (SELECT COUNT(*) FROM STATION) - (SELECT COUNT(DISTINCT CITY) FROM STATION);

```


**output:**


````
13


```