
**[ENG]**

Query a count of the number of cities in CITY having a Population larger than .

![alt text](image.jpg)


**SOLUCIÓN**

```sql


SELECT
    COUNT(name)
FROM
    city
WHERE 
    population > 100000;

```


**output:**


````
6


```