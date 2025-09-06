
# Resposta
```sql
SELECT teacher_id, COUNT(DISTINCT subject_id) as cnt
FROM Teacher
GROUP BY 1
```
## NOTAS

**26-08-25**