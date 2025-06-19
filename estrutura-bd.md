# 🧱 Estrutura de um Banco de Dados Relacional

Um **banco de dados relacional** organiza as informações em **tabelas** que se relacionam entre si. É como uma planilha, mas com regras e lógica por trás. Vamos aos principais elementos:

---

## 📋 Tabelas

- São as **estruturas principais**.
- Armazenam os dados em **linhas (registros)** e **colunas (campos)**.
- Cada tabela representa uma **entidade** (ex: Clientes, Produtos, Pedidos).

---

## 🔑 Chaves

### 🔹 Chave Primária (Primary Key)
- Identifica **unicamente** cada registro.
- Não pode se repetir nem ser nula.
- Exemplo: CPF, ID do cliente.

### 🔹 Chave Estrangeira (Foreign Key)
- Cria uma **ligação** entre tabelas.
- É a **PK de outra tabela** usada como referência.
- Exemplo: ID do cliente na tabela de Pedidos.

---

## 🧩 Relacionamentos

- **1 para 1** (1:1): Um cliente tem um único cadastro adicional.
- **1 para muitos** (1:N): Um cliente pode ter vários pedidos.
- **Muitos para muitos** (N:N): Um aluno pode ter várias disciplinas e vice-versa (nesse caso, usa-se uma tabela intermediária).

---

## 🗃️ Esquema (Schema)

- Representa a **estrutura completa** do banco: tabelas, colunas, tipos de dados, relacionamentos etc.
- Pode ser representado visualmente com **diagramas (DER - Diagrama Entidade Relacionamento)**.

---

## 🧠 Regras importantes

- **Integridade referencial**: garante que os relacionamentos entre tabelas sejam consistentes.
- **Normalização**: técnica para evitar redundância e melhorar a organização dos dados.

---
