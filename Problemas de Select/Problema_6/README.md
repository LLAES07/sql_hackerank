
**[ENG]**
Query the names of all the Japanese cities in the CITY table. The COUNTRYCODE for Japan is JPN.
The CITY table is described as follows:
![alt text](image.png)


**SOLUCIÓN**

```sql
SELECT
    name
FROM
    city
WHERE
    countrycode = 'JPN';
```


**output:**


```
Neyagawa 
Ageo 
Sayama 
Omuta 
Tokuyama 
``` 