# 📈 Função `AVG` no SQL

A função `AVG` retorna a **média dos valores** de uma coluna numérica.

---

## ✅ Exemplo básico

```sql
SELECT AVG(salario) FROM funcionarios;
```

👉 Retorna a **média salarial** da tabela `funcionarios`.

---

## 📊 Média com `GROUP BY`

```sql
SELECT departamento, AVG(salario) AS media_salarial
FROM funcionarios
GROUP BY departamento;
```

👉 Mostra a **média de salário por departamento**.

---

🎓 *Resumo do resumo:*  
`AVG` calcula a média de uma coluna numérica. Ignora valores `NULL`.

---

# 🚀 Função `MAX` no SQL

A função `MAX` retorna o **maior valor** de uma coluna.

---

## ✅ Exemplo básico

```sql
SELECT MAX(salario) FROM funcionarios;
```

👉 Retorna o **maior salário** da tabela.

---

## 📊 Maior valor com `GROUP BY`

```sql
SELECT departamento, MAX(salario) AS maior_salario
FROM funcionarios
GROUP BY departamento;
```

👉 Mostra o **maior salário em cada departamento**.

---

# 🔽 Função `MIN` no SQL

A função `MIN` retorna o **menor valor** de uma coluna.

---

## ✅ Exemplo básico

```sql
SELECT MIN(salario) FROM funcionarios;
```

👉 Retorna o **menor salário** da tabela.

---

## 📊 Menor valor com `GROUP BY`

```sql
SELECT departamento, MIN(salario) AS menor_salario
FROM funcionarios
GROUP BY departamento;
```

👉 Mostra o **menor salário em cada departamento**.

---

🎓 *Resumo das funções agregadas:*

- `AVG()` → calcula a média
- `MAX()` → retorna o maior valor
- `MIN()` → retorna o menor valor
