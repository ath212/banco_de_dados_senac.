# ☕ Banco de Dados – "Cafeteria"
Este repositório contém um projeto de banco de dados desenvolvido em MySQL, utilizando comandos **DDL** e **DML**, com foco em criar e estruturar um sistema simples para uma cafeteria fictícia.
---

## 📘 O que são DDL e DML?

### 🔷 DDL – *Data Definition Language*
São comandos SQL utilizados para **criar** e **modificar** estruturas do banco de dados.

Principais comandos:
- `CREATE` – cria bancos e tabelas
- `ALTER` – modifica tabelas existentes
- `DROP` – exclui tabelas

### 🔶 DML – *Data Manipulation Language*
São comandos que manipulam **os dados dentro das tabelas**.

Principais comandos:
- `INSERT` – insere registros em uma tabela
- `SELECT` – consulta dados de uma tabela
- `UPDATE` – atualiza informações de uma tabela
- `DELETE` – remove registros de uma tabela

---

## 📦 Estrutura do Banco de Dados "Cafeteria"

### **1. Clientes**
- `cliente_id`
- `nome`
- `telefone`
- `email`

### **2. Produtos**
- `produto_id`
- `nome`
- `categoria`
- `preco`
- `estoque`

### **3. Funcionários**
- `funcionario_id`
- `nome`
- `cargo`
- `data_contratacao`

### **4. Pedidos**
- `pedido_id`
- `cliente_id`
- `data_pedido`
- `valor_total`

## ▶️ Como executar o script

1. Abra o **MySQL Workbench**
2. Crie uma nova conexão com o servidor
3. Abra o arquivo `cafeteria.sql`
4. Execute o script completo (⚡ Run)
5. As tabelas serão criadas automaticamente no banco `cafeteria`

## ▶️ Como criar o Diagrama do banco de dados

1. Após a criação do banco de dados, no menu superior do **MySQL Workbench** va na aba  'Database'
2.  <img width="757" height="28" alt="image" src="https://github.com/user-attachments/assets/b97bb125-af23-4125-a60f-8de63590eaa7" />
3. depois va em 'Reverse Engineer'
4. <img width="375" height="26" alt="image" src="https://github.com/user-attachments/assets/4d70c2c1-5dc1-4fba-82fe-7ad632f6ba82" />
. Execute o script completo (⚡ Run)
7. As tabelas serão criadas automaticamente no banco `cafeteria`


---

## 🎯 Objetivo do projeto

Este projeto foi desenvolvido para:

- Praticar comandos DDL (criação e edição de tabelas)
- Entender e Praticar os conceitos de DML (manipulação de dados)
- Desenvolver um modelo de banco relacional simples
---

## 📚 Conteúdo educacional adicionado

O repositório inclui:
- Conceitos de DDL e DML
- Explicações dos comandos básicos
- Modelo estrutural do banco de dados
- Script SQL organizado e comentado
- comandos usado no script.sql e aplicações

---

## 👤 Autor
Projeto criado para fins acadêmicos – SENAC  
Disciplina: Banco de Dados  
