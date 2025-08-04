
**[ENG]**

We define an employee's total earnings to be their monthly ´salay x months´  worked, and the maximum total earnings to be the maximum total earnings for any employee in the Employee table. Write a query to find the maximum total earnings for all employees as well as the total number of employees who have maximum total earnings. Then print these values as  space-separated integers.

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