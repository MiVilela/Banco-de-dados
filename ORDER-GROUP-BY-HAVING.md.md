# 🧮 Comandos `ORDER BY`, `GROUP BY` e `HAVING` no SQL

Esses comandos ajudam a **organizar, agrupar e filtrar** os dados depois que você já usou o `SELECT`.

---

## 🔢 `ORDER BY` – Ordenando os resultados

Usado para **ordenar** os resultados por uma ou mais colunas.

```sql
SELECT nome, idade
FROM clientes
ORDER BY idade DESC;
```

* `ASC` = crescente (padrão)
* `DESC` = decrescente

Você pode ordenar por mais de uma coluna:

```sql
ORDER BY cidade ASC, idade DESC;
```

---

## 👥 `GROUP BY` – Agrupar os dados

Usado para **agrupar os resultados** com base em uma ou mais colunas.
Geralmente usado junto com **funções agregadas** (`COUNT`, `SUM`, `AVG`, etc.).

```sql
SELECT cidade, COUNT(*) AS total_clientes
FROM clientes
GROUP BY cidade;
```

👉 Aqui estamos contando quantos clientes existem em cada cidade.

---

## 🧼 `HAVING` – Filtrar após o agrupamento

`HAVING` é parecido com `WHERE`, **mas é usado depois do `GROUP BY`**.
Serve para **filtrar grupos**, e não linhas individuais.

```sql
SELECT cidade, COUNT(*) AS total_clientes
FROM clientes
GROUP BY cidade
HAVING COUNT(*) > 5;
```

👉 Isso mostra apenas as cidades com **mais de 5 clientes**.

---

## 🎯 Diferença entre `WHERE` e `HAVING`

| `WHERE`  | filtra linhas antes do `GROUP BY`  |
| -------- | ---------------------------------- |
| `HAVING` | filtra grupos depois do `GROUP BY` |

---
