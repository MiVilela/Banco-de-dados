# 🔍 Comando `SELECT` no SQL

O comando `SELECT` é usado para **consultar dados** em uma ou mais tabelas do banco de dados.  
Pensa nele como: *"me mostra esses dados aqui!"*

---

## 🧱 Estrutura básica

```sql
SELECT colunas
FROM tabela;
```
Exemplo:
```sql
SELECT nome, idade
FROM clientes;
```

👉 Isso vai trazer apenas as colunas nome e idade da tabela clientes.

## 🎯 Usando o * (asterisco)
```sql
SELECT * FROM clientes;
```
- Traz todas as colunas da tabela.

- Útil em testes ou quando você quer ver "tudo de uma vez".

## 🎛️ Filtrando dados com `WHERE`
```sql
SELECT nome
FROM clientes
WHERE idade >= 18;
```
- Mostra apenas clientes com 18 anos ou mais.

- O `WHERE` serve para filtrar os resultados com base em alguma condição.

## 🧮 Funções agregadas
```sql
SELECT COUNT(*) FROM clientes;
SELECT AVG(idade) FROM clientes;
SELECT MAX(idade) FROM clientes;
```
`COUNT(*)`: conta quantos registros existem.

`AVG(coluna)`: média dos valores.

`MAX, MIN, SUM`: maior, menor e soma.

## 🧹 Ordenando com ORDER BY
```sql
SELECT nome, idade
FROM clientes
ORDER BY idade DESC;
```
- Ordena os resultados pela coluna `idade`.

- `ASC` = crescente (padrão), `DESC` = decrescente.

## 🔢 Limitando resultados
```sql
SELECT nome
FROM clientes
LIMIT 5;
```
- Mostra só os 5 primeiros resultados.
