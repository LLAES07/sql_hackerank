
**[ENG]**

Query the list of CITY names from STATION that do not start with vowels and do not end with vowels. Your result cannot contain duplicates.



![alt text](image.jpg)


**SOLUCIÓN**

```sql

SELECT
    DISTINCT (city)
FROM
    station
WHERE 
    lower(city) NOT REGEXP '^[aeiou]' AND
    lower(city) NOT REGEXP '[aeiou]$';

```


**output:**


```
Baker 
Baldwin 
Bass Harbor 
Beaufort 
Beaver Island 
Benedict 
Bennington 
Berryton 
Beverly 
Bison 
Blue River 
Bowdon 
Bowdon Junction 
Bridgeport 
Bridgton 
Brighton 
Brilliant 
Bristol 
Brownstown 

```