# Tarefa 01

## Apresentação Pessoal

Olá! Meu nome é Jonathas Nóbrega da Silva, sou desenvolvedor Full Stack e tenho experiência sólida em tecnologias como **React** e **Node.js**, que utilizo diariamente no desenvolvimento de aplicações web modernas. Também possuo um bom domínio de **Python**, especialmente com o framework **Flask**, além de conhecimentos em **Java** e **Lua**.

Participei de uma startup chamada BruxLevel por 6 meses, onde pude vivenciar o ambiente dinâmico de uma empresa em fase inicial, contribuindo ativamente para o desenvolvimento de soluções tecnológicas. Atualmente, estou há mais de 1 ano atuando como estagiário na empresa _Clair & Leitão - Contabilidade Pública_, exercendo a função de desenvolvedor Full Stack e trabalhando principalmente com **React** e **Node.js**.

Tenho afinidade com o desenvolvimento de software e estou sempre em busca de aprimorar minhas habilidades tanto no backend quanto no frontend, buscando criar soluções eficientes e bem estruturadas.

# Banco de Dados Relacional, SQL, SGBD e Normalização

## 📚 O que é um Banco de Dados Relacional?

Um **Banco de Dados Relacional (BDR)** é um modelo de banco de dados que organiza os dados em **tabelas**, compostas por **linhas (registros)** e **colunas (atributos)**.

Cada **tabela** representa uma entidade (exemplo: clientes, produtos, pedidos) e cada **linha** representa uma ocorrência específica dessa entidade.

Exemplo:  
Uma tabela `clientes` pode ter colunas como `id`, `nome`, `email`, e cada linha representaria um cliente específico.

---

## 🔎 O que é SQL?

**SQL (Structured Query Language)** é a **linguagem padrão** usada para trabalhar com bancos de dados relacionais.

Com o SQL, podemos:

- **Criar tabelas**
- **Inserir dados**
- **Consultar informações**
- **Atualizar registros**
- **Excluir dados**
- Entre outras operações.

### Exemplo básico de consulta SQL:

```sql
SELECT nome, email FROM clientes WHERE cidade = 'São Paulo';
```

---

## 🖥️ O que é SGBD?

**SGBD (Sistema de Gerenciamento de Banco de Dados)** é o software responsável por:

- **Armazenar os dados**
- **Gerenciar as tabelas**
- **Garantir a segurança e integridade dos dados**
- **Fornecer uma interface entre o usuário e o banco de dados**

### Exemplos de SGBDs relacionais:

- MySQL
- PostgreSQL
- SQLite
- Oracle Database
- Microsoft SQL Server

---

## 🏗️ O que é Normalização?

A **normalização** é um processo de organização das tabelas de um banco de dados para:

- **Eliminar redundâncias (dados repetidos)**
- **Evitar anomalias de inserção, atualização e exclusão**
- **Garantir a integridade dos dados**

Esse processo é dividido em etapas chamadas de **Formas Normais (FNs)**, cada uma com regras específicas que tornam o banco de dados mais eficiente e organizado.

---

## 📋 Exemplo prático: Normalização até a 2ª Forma Normal (2FN)

### ❌ Exemplo de tabela mal estruturada (violando a 2FN):

Neste exemplo, a tabela armazena os produtos de um pedido, mas os campos `nome_produto` e `preço_unitário` dependem apenas de `produto_id`, não da chave composta inteira (`pedido_id + produto_id`):

| pedido_id | produto_id | nome_produto | preço_unitário |
| --------- | ---------- | ------------ | -------------- |
| 101       | 10         | Teclado      | 150.00         |
| 101       | 11         | Mouse        | 80.00          |
| 102       | 10         | Teclado      | 150.00         |

**Problema:**  
Se o preço do produto mudar, será necessário alterar em vários lugares, gerando risco de inconsistência.

---

### ✅ Aplicando a 2FN (Segunda Forma Normal):

**Solução:**  
Separar os dados dependentes em duas tabelas:

### Tabela: pedidos_produtos

Esta tabela representa o relacionamento entre pedidos e produtos:

| pedido_id | produto_id |
| --------- | ---------- |
| 101       | 10         |
| 101       | 11         |
| 102       | 10         |

### Tabela: produtos

Esta tabela armazena os dados fixos de cada produto:

| produto_id | nome_produto | preço_unitário |
| ---------- | ------------ | -------------- |
| 10         | Teclado      | 150.00         |
| 11         | Mouse        | 80.00          |

---

## ✅ Benefícios da Normalização

- **Menor redundância de dados**
- **Facilidade de manutenção**
- **Maior consistência**
- **Evita anomalias de inserção, exclusão e atualização**

---

## ✅ Resumo Geral

Um **Banco de Dados Relacional** organiza os dados em **tabelas**, com **linhas (registros)** e **colunas (atributos)**.

O **SQL** é a linguagem usada para **criar, consultar e manipular dados** nesses bancos.

Um **SGBD** é o software que **gerencia o banco de dados**, como o MySQL ou PostgreSQL.

A **normalização** é uma prática essencial para **organizar os dados**, **evitar duplicidade** e garantir a **integridade** das informações.

---
