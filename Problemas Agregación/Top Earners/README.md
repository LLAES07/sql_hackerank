
**[ENG]**

We define an employee's total earnings to be their monthly ´salay x months´  worked, and the maximum total earnings to be the maximum total earnings for any employee in the Employee table. Write a query to find the maximum total earnings for all employees as well as the total number of employees who have maximum total earnings. Then print these values as  space-separated integers.

**[ESP]**

Definimos las ganancias totales de un empleado como su salario mensual multiplicado por la cantidad de meses trabajados, y las ganancias totales máximas como las mayores ganancias totales de cualquier empleado en la tabla Employee. Escribe una consulta para encontrar las ganancias totales máximas de todos los empleados, así como el número total de empleados que tienen esas ganancias totales máximas. Luego imprime estos valores como enteros separados por un espacio.

![alt text](image.png)


**SOLUCIÓN**

```sql

SELECT 
    MAX(salary * months) AS max_earnings,
    COUNT(*) AS num_employees
FROM 
    Employee
WHERE 
    (salary * months) = (SELECT MAX(salary * months) FROM Employee);

```


**output:**


````

108064 7 


```