
**[ENG]**
Given the CITY and COUNTRY tables, query the names of all the continents (COUNTRY.Continent) and their respective average city populations (CITY.Population) rounded down to the nearest integer.

Note: CITY.CountryCode and COUNTRY.Code are matching key columns.

![alt text](image1.jpg)
![alt text](image2.jpg)

**SOLUCIÓN**

```sql

SELECT
    ct.continent,
    FLOOR(AVG(c.population)) AS avg_pop_by_continent
FROM
    city c
INNER JOIN
    country ct
ON 
    c.countrycode = ct.code
GROUP BY
    ct.continent;



````


**output:**


````
Oceania 109189 
South America 147435 
Europe 175138 
Africa 274439 
Asia 693038

```