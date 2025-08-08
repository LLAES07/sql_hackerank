
**[ENG]**

Query the sum of the populations for all Japanese cities in CITY. The COUNTRYCODE for Japan is JPN.

**[ES]**

Haz una consulta para conocer la suma de la población total de todas las ciudades japonesas en la tabla city. El countrycode de japon es JPN.

![alt text](image.jpg)


**SOLUCIÓN**

```sql
SELECT CEIL(
    AVG(salary) - 
    AVG(CAST(REPLACE(CAST(salary AS CHAR), '0', '') AS UNSIGNED))
) AS error
FROM employees;


```


**output:**


````

2253



```