
**[ENG]**

Query the sum of the populations for all Japanese cities in CITY. The COUNTRYCODE for Japan is JPN.



![alt text](image.jpg)


**SOLUCIÓN**

```sql

SELECT
    SUM(population) AS total_jpn_pop
FROM
    city
WHERE
    countrycode LIKE 'JPN';


```


**output:**


````

454250



```