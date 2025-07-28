
**[ENG]**

Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates.



**SOLUCIÓN**

```sql

SELECT 
    DISTINCT(city)
FROM
    station
WHERE
    lower(city) NOT REGEXP '^[aeiou]';


```


**output:**


````
Baileyville 
Bainbridge 
Baker 
Baldwin 
Barrigada 
Bass Harbor 
Baton Rouge 
Bayville 
Beaufort 
Beaver Island 
Bellevue 
Benedict 
Bennington 
Bentonville 
Berryton 
Bertha 
Beverly 
Biggsville 
Bison 

```