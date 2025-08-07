
**[ENG]**

Given the CITY and COUNTRY tables, query the sum of the populations of all cities where the CONTINENT is 'Asia'.

Note: CITY.CountryCode and COUNTRY.Code are matching key columns.

Input Format

![alt text](image1.jpg)
![alt text](image2.jpg)

**SOLUCIÓN**

```sql


SELECT
    SUM(population) AS total_pop_asia
FROM
    city c
INNER JOIN (SELECT
                DISTINCT (CODE)
            FROM
                country
            WHERE
                lower(continent) = 'asia') AS t2 
ON 
    c.countrycode = t2.code



````


**output:**


````




```