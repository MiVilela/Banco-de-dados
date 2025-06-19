# ➕ Função `SUM` no SQL

A função `SUM` serve para **somar os valores** de uma coluna numérica.  
É tipo perguntar: *"qual o total disso tudo aqui?"*

---

## ✅ Exemplo básico

```sql
SELECT SUM(valor_compra) FROM vendas;
```

👉 Soma todos os valores da coluna `valor_compra` na tabela `vendas`.

---

## 🎯 Somando com condição

```sql
SELECT SUM(valor_compra)
FROM vendas
WHERE cliente_id = 10;
```

👉 Soma todas as compras feitas pelo cliente de ID 10.

---

## 📊 Usando com `GROUP BY`

```sql
SELECT cliente_id, SUM(valor_compra) AS total_gasto
FROM vendas
GROUP BY cliente_id;
```

👉 Mostra quanto cada cliente gastou no total.

---

🎓 *Resumo do resumo:*  
`SUM` serve para somar valores numéricos.

- Pode ser usado com `WHERE` para filtrar somas  
- Funciona muito bem com `GROUP BY` para somar por categoria
- Ignora valores `NULL` automaticamente
