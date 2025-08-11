
**[ENG]**
Query a list of CITY and STATE from the STATION table.
The STATION table is described as follows:
where LAT_N is the northern latitude and LONG_W is the western longitude.

**[ESP]**  
Consulta una lista de CITY y STATE de la tabla STATION.  
La tabla STATION se describe de la siguiente manera:

donde LAT_N es la latitud norte y LONG_W es la longitud oeste.

![alt text](image.png)

**SOLUCIÓN**

```sql
SELECT
    city,
    state

FROM
    station;
```


**output:**


```
Acme LA 
Addison MI 
Agency MO 
Aguanga CA 
Alanson MI 
Alba MI 
Albany CA 
Albion IN 
Algonac MI 
Aliso Viejo CA 
Allerton IA 
Alpine AR 
Alton MO 
Amazonia MO 
Amo IN 
Andersonville GA 
Andover CT 
Anthony KS 
Archie MO 
Arispe IA {-truncated-}

``` 