
# Resposta
```sql
SELECT
    employee_id
FROM Employees
WHERE
    manager_id NOT IN (SELECT employee_id FROM employees) 
    AND salary <30000
ORDER BY 1
```
**26-08-25**