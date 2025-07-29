
**[ENG]**

Query the list of CITY names from STATION that either do not start with vowels or do not end with vowels. Your result cannot contain duplicates.


![alt text](image.jpg)

**SOLUCIÓN**

```sql

SELECT
    DISTINCT (city)
FROM
    station
WHERE 
    lower(city) NOT REGEXP '^[aeiou]' OR
    lower(city) NOT REGEXP '[aeiou]$';

```


**output:**


```
Addison 
Agency 
Alanson 
Albany 
Albion 
Algonac 
Allerton 
Alton 
Andover 
Anthony 
Arlington 
Arrowsmith 
Athens 
Auburn 
Baileyville 
Bainbridge 
Baker 
Baldwin 
Barrigada 
Bass Harbor {-truncated-}
```