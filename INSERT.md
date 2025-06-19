# 📝 Comando `INSERT` no SQL

O comando `INSERT` é usado para **inserir novos dados** (registros) em uma tabela.  
É tipo dizer pro banco: *"ô, guarda isso aqui pra mim!"*

---

## 🧱 Estrutura básica

```sql
INSERT INTO nome_tabela (coluna1, coluna2, ...)
VALUES (valor1, valor2, ...);
```
Exemplo:

```sql
INSERT INTO clientes (nome, idade, cidade)
VALUES ('Ana', 25, 'Curitiba');
```
👉 Isso insere uma nova cliente chamada Ana, com 25 anos, da cidade de Curitiba.

## ⚠️ Cuidados importantes

- A ordem dos valores deve seguir a ordem das colunas.

- Os valores de texto (strings) precisam estar entre aspas simples: `exemplo`.

## 🙈 Inserindo em todas as colunas

Se você vai preencher todas as colunas da tabela, pode omitir a lista de colunas:

```sql
INSERT INTO clientes
VALUES (1, 'Carlos', 30, 'São Paulo');
```
⚠️ Atenção: a ordem dos valores precisa ser exatamente a mesma da estrutura da tabela!

## 📦 Inserindo múltiplas linhas de uma vez

```sql
INSERT INTO clientes (nome, idade, cidade)
VALUES 
  ('João', 20, 'Londrina'),
  ('Marina', 28, 'Belo Horizonte'),
  ('Paulo', 22, 'Recife');
```
- Insere vários registros de uma vez só.

## 🚫 Inserção com erro comum
Se você tentar inserir um valor em uma coluna que não permite NULL (vazio), ou que já tem uma chave primária duplicada, o banco vai reclamar!
