
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
-- 1ER paso generar un row_number
WITH ranking1 AS (
                    SELECT
                        name,
                        occupation,
                        ROW_NUMBER() OVER(PARTITION BY occupation ORDER BY name ASC) as rking
                    FROM
                        occupations
                )

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