
# Resposta
```sql
SELECT 
    user_id,
    UPPER(SUBSTRING(NAME,1,1)) || LOWER(SUBSTRING(NAME, 2)) as name
FROM Users
ORDER BY user_id
```
## NOTAS
fiz com left() e right() e deu certo, mas não tinha a msm performace que  usando substring, adoro esse tipo de questão que aprendo coisa nova!

**22-09-25**