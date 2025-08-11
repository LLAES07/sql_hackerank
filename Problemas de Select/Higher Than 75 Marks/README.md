
**[ENG]**

Query the Name of any student in STUDENTS who scored higher than 75 Marks. Order your output by the last three characters of each name. If two or more students both have names ending in the same last three characters (i.e.: Bobby, Robby, etc.), secondary sort them by ascending ID.

**[ESP]**  
Consulta el Nombre de cualquier estudiante en la tabla STUDENTS que haya obtenido más de 75 puntos. Ordena tu resultado por los últimos tres caracteres de cada nombre. Si dos o más estudiantes tienen nombres que terminan con los mismos tres últimos caracteres (por ejemplo: Bobby, Robby, etc.), ordénalos en segundo lugar por ID en orden ascendente.

![alt text](image.png)


**SOLUCIÓN**

```sql
SELECT
    name
FROM 
    students
WHERE 
    marks > 75
ORDER BY 
    RIGHT(name, 3), 
    id ASC;    

```


**output:**


````
Stuart 
Kristeen 
Christene 
Amina 
Aamina 
Priya 
Heraldo 
Scarlet 
Julia 
Salma 
Britney 
Priyanka 
Samantha 
Vivek 
Belvet 
Devil 



```