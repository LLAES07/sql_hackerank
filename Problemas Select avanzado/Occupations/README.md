
**[ENG]**
Pivot the Occupation column in OCCUPATIONS so that each Name is sorted alphabetically and displayed underneath its corresponding Occupation. The output should consist of four columns (Doctor, Professor, Singer, and Actor) in that specific order, with their respective names listed alphabetically under each column.

Note: Print NULL when there are no more names corresponding to an occupation.

Input Format

The OCCUPATIONS table is described as follows:



![alt text](img1.jpg)

Occupation will only contain one of the following values: Doctor, Professor, Singer or Actor.



![alt text](img2.jpg)

**SOLUCIÓN**



```sql
-- 1ER paso generar un row_number seleccionando nombre, ocupación. Agregamos una columna nueva para poder ordenar alfabeticamente los nombres 
WITH ranking1 AS (
                    SELECT
                        name,
                        occupation,
                        ROW_NUMBER() OVER(PARTITION BY occupation ORDER BY name ASC) as rking
                    FROM
                        occupations
                )


/*
Ahora con el ranking listo agrupamos las filas por cada ranking para que cada ocupación se quede alineada en forma de columnas y cada una de estas tenga solo un ranking 1, 2, 3, etc. En este caso utilizamos MAX(CASE) para poder transformar las filas a columnas y en caso de una ocupacion no estar dentro de esta es NULL.
*/
SELECT
    MAX(CASE
        WHEN occupation = 'Doctor' THEN name end)  as Doctor,
    MAX(CASE
        WHEN occupation = 'Professor' THEN name end) as Professor,
    MAX(CASE
        WHEN occupation = 'Singer' THEN name end) as Singer,
    MAX(CASE
        WHEN occupation = 'Actor' THEN name end) as Actor
FROM
    ranking1
GROUP BY rking;
````


**output:**




````
Aamina Ashley Christeen Eve 
Julia Belvet Jane Jennifer 
Priya Britney Jenny Ketty 
NULL Maria Kristeen Samantha 
NULL Meera NULL NULL 
NULL Naomi NULL NULL 
NULL Priyanka NULL NULL

```