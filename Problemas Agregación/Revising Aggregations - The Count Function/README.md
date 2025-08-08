
**[ENG]**

Query a count of the number of cities in CITY having a Population larger than .

**[ESP]**

Consulta un conteo del número de ciudades en CITY que tienen una población mayor que .

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