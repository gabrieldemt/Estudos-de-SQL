
# Resposta
```sql
SELECT
    contest_id,
    ROUND(COUNT(DISTINCT user_id) * 100.0 / (SELECT COUNT(DISTINCT user_id) FROM Users), 2) as percentage
FROM Register
GROUP BY contest_id
ORDER BY percentage DESC, contest_id ASC
```
## NOTAS
Conta basica de porcentagem, pelo oque vi no leetcode após responder, percebi que esse codigo não é muito performatico

**27-08-25**