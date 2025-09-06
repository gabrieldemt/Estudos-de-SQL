
# Resposta
```sql
SELECT 
    to_char(trans_date, 'yyyy-mm') AS month, country,
    COUNT(DISTINCT ID) as trans_count,
    COUNT(CASE WHEN state = 'approved' THEN 1 ELSE NULL END) AS approved_count,
    SUM(amount) AS trans_total_amount,
    SUM(CASE WHEN state = 'approved' THEN amount ELSE 0 END) AS approved_total_amount
FROM Transactions
GROUP BY month, country
```
## NOTAS
Primeira vez que preciso usar CASE WHEN, tão simples, mas na faculdade não foi cobrado, então tive dificuldade, tive que apelar para VER a solução!! exatamente, fui atrás da solução e de entender como funciona, até por que eu não preciso "reinventar" e fazer do meu jeito, as vezes é só aprender e ganhar repertorio pra uma proxima questão.

A titulo de curiosidade, a disciplina de banco de dados que fiz foi modelagem de banco de dados, então boa parte foi teorica, e chegando na metade pro final que entramos no SQL, acho que gostei do jeito que foi, pois 
tenho uma base legal, mesmo sendo um aprendizado mais demorado...
A pratica mesmo vem agora
**30-08-25**