
**[ENG]**
Given the CITY and COUNTRY tables, query the names of all cities where the CONTINENT is 'Africa'.

Note: CITY.CountryCode and COUNTRY.Code are matching key columns.


![alt text](image1.jpg)
![alt text](image2.jpg)

**SOLUCIÓN**

```sql




SELECT
    DISTINCT(c.name)
FROM
    city c
INNER JOIN
    country  ct
    ON 
        c.countrycode = ct.code
WHERE
    LOWER(ct.continent) = 'africa'


````


**output:**


````

Qina 
Warraq al-Arab 
Kempton Park 
Alberton 
Klerksdorp 
Uitenhage 
Brakpan 
Libreville 


```