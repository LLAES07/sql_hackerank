
**[ENG]**

Query the average population for all cities in CITY, rounded down to the nearest integer.

**[ESP]**

Consulta la población promedio de todas las ciudades en CITY, redondeada hacia abajo al número entero más cercano.

![alt text](image.jpg)


**SOLUCIÓN**

```sql
SELECT 
    FLOOR(AVG(population)) AS average_population
FROM 
    city;


```


**output:**


````

454250



```