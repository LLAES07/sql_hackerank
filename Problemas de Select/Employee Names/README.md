
**[ENG]**

Write a query that prints a list of employee names (i.e.: the name attribute) from the Employee table in alphabetical order.
**[ESP]**  
Escribe una consulta que imprima una lista de nombres de empleados (es decir, el atributo name) de la tabla Employee en orden alfabético.



![alt text](image.png)


**SOLUCIÓN**

```sql

SELECT 
    name
FROM
    employee
ORDER BY name ASC;

```


**output:**


````
Alan 
Amy 
Andrew 
Andrew 
Angela 
Ann 
Anna 
Anthony 
Antonio 
Benjamin 
Bonnie 
Brandon 
Brandon 
Brian 
Carol 
Charles 
Christina 
Christina 
Christine 
Christine {-truncated-}

```