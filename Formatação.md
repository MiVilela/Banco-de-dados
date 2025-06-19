# 🧩 Concatenando Colunas no SQL

Concatenar colunas é o processo de **juntar textos de diferentes colunas** em um só resultado.  
É muito usado pra criar nomes completos, endereços, etc.

---

## ✅ Exemplo usando `+` (SQL Server)

```sql
SELECT nome + ' - ' + sobrenome AS nome_completo
FROM produtos;
```

👉 Junta o nome e o sobrenome separados por um traço.

---

# 🔤 Funções `UPPER` e `LOWER` no SQL Server

Essas funções servem para **alterar o formato de letras** em colunas de texto.

---

## 🔼 `UPPER` → deixa tudo em MAIÚSCULO

```sql
SELECT UPPER(nome) AS nome_maiusculo FROM clientes;
```

👉 Transforma "ana" em "ANA".

---

## 🔽 `LOWER` → deixa tudo em minúsculo

```sql
SELECT LOWER(nome) AS nome_minusculo FROM clientes;
```

👉 Transforma "CARLOS" em "carlos".

---

🎯 Pode ser útil para **padronizar dados** ou fazer comparações sem se preocupar com caixa (maiúsculas/minúsculas).

---

🎓 *Resumo do resumo:*  
- `UPPER(coluna)` → tudo maiúsculo
- `LOWER(coluna)` → tudo minúsculo

# 📅 Formatando Datas no SQL Server

No SQL Server, você pode formatar datas com a função `FORMAT()`.

---

## ✅ Exemplo básico

```sql
SELECT FORMAT(data_nascimento, 'dd/MM/yyyy') AS data_formatada
FROM clientes;
```

👉 Mostra a data no formato brasileiro: **dia/mês/ano**.

---

## 🧠 Outros exemplos úteis

```sql
-- Data por extenso
SELECT FORMAT(GETDATE(), 'dd MMMM yyyy', 'pt-BR') AS data_extenso;

-- Só ano e mês
SELECT FORMAT(GETDATE(), 'yyyy-MM') AS ano_mes;
```

---
