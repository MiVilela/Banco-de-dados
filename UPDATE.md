# ✏️ Comando `UPDATE` no SQL

O `UPDATE` serve para **alterar dados existentes** em uma tabela.  
Você escolhe qual campo mudar, e em qual registro isso deve acontecer.

---

## 🧱 Estrutura básica

```sql
UPDATE nome_tabela
SET coluna1 = valor1, coluna2 = valor2
WHERE condição;
```
Exemplo:

```sql
UPDATE clientes
SET idade = 26
WHERE nome = 'Ana';
```
👉 Isso vai atualizar a idade da cliente chamada Ana para 26.

## ⚠️ Cuidado com o `WHERE`
Se você esquecer o `WHERE`, ele vai atualizar todos os registros da tabela!
```sql
UPDATE clientes
SET cidade = 'São Paulo';
```
Isso mudaria a cidade de todos os clientes pra São Paulo.

## ✨ Atualizando múltiplos campos
```sql
UPDATE clientes
SET idade = 30, cidade = 'Curitiba'
WHERE nome = 'Carlos';
```
- Você pode atualizar várias colunas de uma vez.

- Só separar com vírgulas.
