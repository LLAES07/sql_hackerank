
**[ENG]**

Query the list of CITY names ending with vowels (a, e, i, o, u) from STATION. Your result cannot contain duplicates.




![alt text](image.png)

**SOLUCIÓN**

```sql

SELECT
    DISTINCT(city)
FROM
    station
WHERE
    lower(city) LIKE '%a' or
    lower(city) LIKE '%e' or
    lower(city) LIKE '%i' or
    lower(city) LIKE '%o' or
    lower(city) LIKE '%u';   


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
Baileyville 
Bainbridge 
Barrigada 
Baton Rouge 
Bayville 
Bellevue 
Bentonville 
Bertha {-truncated-}
```