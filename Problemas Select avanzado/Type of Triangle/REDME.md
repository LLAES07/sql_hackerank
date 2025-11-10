
**[ENG]**
Write a query identifying the type of each record in the TRIANGLES table using its three side lengths. Output one of the following statements for each record in the table:

- Equilateral: It's a triangle with  sides of equal length.
- Isosceles: It's a triangle with  sides of equal length.
- Scalene: It's a triangle with  sides of differing lengths.
- Not A Triangle: The given values of A, B, and C don't form a triangle.
The TRIANGLES table is described as follows:

![alt text](img1.jpg)

Each row in the table denotes the lengths of each of a triangle's three sides.

Sample Input


![alt text](sample_input.jpg)

**SOLUCIÓN**

Primero tenemos que tener presente que para que se pueda formar un triangulo se debe cumplir la desigualdad triangular 

\[A + B > C, \quad A + C > B, \quad B + C > A\]

Por lo que para que no sea un triangulo no se debe cumplir esta condición

```sql

SELECT
    CASE
        WHEN A + B <= C OR A + C <= B OR B + C <= A THEN 'Not A Triangle' 
        WHEN A = B AND B = C THEN 'Equilateral'
        WHEN A = B OR B = C OR C = A THEN 'Isosceles'
        ELSE 'Scalene'
    END AS tipo_triangulo
FROM
    TRIANGLES;

````


**output:**




````
Equilateral 
Equilateral 
Isosceles 
Equilateral 
Isosceles 
Equilateral 
Scalene 
Not A Triangle 
Scalene 
Scalene 
Scalene 
Not A Triangle 
Not A Triangle 
Scalene 
Equilateral


```