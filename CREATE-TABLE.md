# 🧱 Comando `CREATE TABLE` no SQL

O comando `CREATE TABLE` serve para **criar uma nova tabela** no banco de dados.  
É onde você define os **campos (colunas)**, os **tipos de dados** e até algumas **regras**.

---

## 🧱 Estrutura básica

```sql
CREATE TABLE nome_tabela (
  coluna1 tipo1 restrições,
  coluna2 tipo2 restrições,
  ...
);
```
Exemplo simples:
```sql
CREATE TABLE clientes (
  id INT PRIMARY KEY,
  nome VARCHAR(100),
  idade INT,
  cidade VARCHAR(50)
);
```
👉 Isso cria a tabela clientes com 4 colunas:

- id: número inteiro, chave primária

- nome: texto de até 100 caracteres

- idade: número inteiro

- cidade: texto de até 50 caracteres

## 🧠 Tipos de dados comuns
| Tipo           | Descrição                        |
| -------------- | -------------------------------- |
| `INT`          | Número inteiro                   |
| `VARCHAR(n)`   | Texto com até *n* caracteres     |
| `DATE`         | Data (ex: '2025-06-17')          |
| `DECIMAL(x,y)` | Número com casas decimais        |
| `BOOLEAN`      | Verdadeiro ou falso (true/false) |

## 🔐 Restrições comuns
- `PRIMARY KEY` → identifica de forma única cada linha

- `NOT NULL` → obriga a preencher o campo

- `UNIQUE` → valor não pode se repetir

- `DEFAULT` → valor padrão

- `FOREIGN KEY` → cria relação com outra tabela

## 🧩 Exemplo com chave estrangeira
```sql
CREATE TABLE pedidos (
  id INT PRIMARY KEY,
  cliente_id INT,
  data DATE,
  FOREIGN KEY (cliente_id) REFERENCES clientes(id)
);
```
👉 Aqui o campo `cliente_id` se conecta com o campo `id` da tabela `clientes`.
