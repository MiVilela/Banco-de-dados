# 🗑️ Comando `DELETE` no SQL

O comando `DELETE` é usado para **remover dados** (linhas) de uma tabela.  

---

## 🧱 Estrutura básica

```sql
DELETE FROM nome_tabela
WHERE condição;
```
Exemplo:
```sql
DELETE FROM clientes
WHERE nome = 'João';
```
👉 Isso apaga o cliente chamado João da tabela.

## ⚠️ PERIGO: Sem `WHERE`, ele apaga tudo!

```sql
DELETE FROM clientes;
```
🚨 Essa instrução remove TODAS as linhas da tabela `clientes`.

Nunca use `DELETE` sem `WHERE`, a menos que você realmente queira limpar toda a tabela.

## 🧪 Sempre teste com `SELECT` antes
```sql
SELECT * FROM clientes WHERE nome = 'João';
```
Veja quem será apagado antes de executar o `DELETE`.
