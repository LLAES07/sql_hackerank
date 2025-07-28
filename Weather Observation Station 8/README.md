
**[ENG]**

Query the list of CITY names from STATION which have vowels (i.e., a, e, i, o, and u) as both their first and last characters. Your result cannot contain duplicates.

![alt text](image.jpg)
**SOLUCIÓN**

```sql


SELECT  
    city
FROM
    station
    
WHERE 
    lower(city) REGEXP '^[aeiou]' AND
    lower(city) REGEXP '[aeiou]$';

    

```


**output:**


````
Acme 
Aguanga 
Alba 
Aliso Viejo 
Alpine 
Amazonia 
Amo 
Andersonville 
Archie 
Arispe 
Arkadelphia 
Atlantic Mine 
East China 
East Irvine 
Eastlake 
Eleele 
Elm Grove 
Eriline 
Ermine 
Eskridge {-truncated-}


```