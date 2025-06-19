# 🔢 Função `COUNT` no SQL

A função `COUNT` serve para **contar registros** em uma tabela.  
É tipo perguntar: *"quantas linhas tem aqui?"*

---

## ✅ Exemplo básico

```sql
SELECT COUNT(*) FROM clientes;
```

👉 Conta **todas as linhas** da tabela `clientes`.

---

## 🎯 Contando com condição

```sql
SELECT COUNT(*) 
FROM clientes 
WHERE cidade = 'São Paulo';
```

👉 Conta quantos clientes são de **São Paulo**.

---

## 🆔 Contando valores NÃO NULOS de uma coluna

```sql
SELECT COUNT(email) FROM clientes;
```

👉 Conta quantas pessoas **têm e-mail cadastrado** (ignora valores `NULL`).

---

## 🧐 Usando com `GROUP BY`

```sql
SELECT cidade, COUNT(*) AS total_clientes
FROM clientes
GROUP BY cidade;
```

👉 Mostra quantos clientes existem **em cada cidade**.

---

🎓 *Resumo do resumo:*  
`COUNT` serve pra contar registros.

- `COUNT(*)` → conta tudo  
- `COUNT(coluna)` → conta só valores não nulos  
- Pode usar junto com `WHERE`, `GROUP BY`, `HAVING`, etc.
