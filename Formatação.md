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

# 🔑 Chaves Primárias e Estrangeiras no SQL

## 🆔 PRIMARY KEY (Chave Primária)

A `PRIMARY KEY` é usada para **identificar unicamente** cada linha de uma tabela.  
Pensa nela como o "CPF" de cada registro.

---

### ✅ Exemplo:

```sql
CREATE TABLE clientes (
    cliente_id INT PRIMARY KEY,
    nome VARCHAR(100)
);
```

👉 A coluna `cliente_id` será única e **não pode ser nula** (`NOT NULL` implícito).

---

## 🔗 FOREIGN KEY (Chave Estrangeira)

A `FOREIGN KEY` serve para **ligar duas tabelas**.  
Ela cria uma **relação entre um campo de uma tabela e a `PRIMARY KEY` de outra**.

---

### ✅ Exemplo:

```sql
CREATE TABLE pedidos (
    pedido_id INT PRIMARY KEY,
    cliente_id INT,
    FOREIGN KEY (cliente_id) REFERENCES clientes(cliente_id)
);
```

👉 Aqui, `cliente_id` em `pedidos` aponta para `cliente_id` em `clientes`.

---

## 📌 Por que usar?

- **Integridade referencial**: garante que o valor da chave estrangeira **exista na tabela pai**
- Ajuda a manter os dados **organizados e coerentes**
- Permite criar **relações entre tabelas**

---

🎓 *Resumo do resumo:*  
- `PRIMARY KEY` → identifica unicamente um registro  
- `FOREIGN KEY` → conecta tabelas e mantém integridade dos dados  
- Juntas, formam a base dos **bancos de dados relacionais**

---

