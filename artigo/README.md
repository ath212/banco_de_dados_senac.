# Tipos de Dados e Regras de Integridade na Modelagem SQL: Guia Completo com Exemplos

## Introdução
A modelagem de dados é um processo essencial no projeto de bancos de dados e sistemas de informação, pois ela envolve a criação de representações estruturadas e organizadas dos dados que uma organização precisa armazenar, acessar e gerenciar.
A modelagem de dados é fundamental para garantir que os dados sejam armazenados de forma eficaz, facilmente acessíveis e mantenham a integridade e a consistência.
Dessa maneira, a modelagem de dados desempenha um papel essencial na criação de sistemas de informação eficientes e confiáveis.

---

## Tipos de Dados em SQL
Os tipos de dados determinam o tipo de informação que pode ser armazenada em uma tabela de banco de dados. Eles ajudam o sistema a organizar, validar e manipular os dados corretamente.

### Numéricos (INT, DECIMAL, FLOAT)
- **INT**: usado para números inteiros, como quantidade de itens, idade, ou códigos sem casas decimais.
- **DECIMAL**: especifica números com casas decimais fixas, ideal quando precisa de precisão, como valores financeiros ou medições exatas.
- **FLOAT**: permite números com casas decimais flutuantes, ótimo para valores científicos ou resultados aproximados, mas pode perder precisão em algumas situações.

### Tipos Numéricos Exatos no SQL Server
Os tipos numéricos exatos no SQL Server são essenciais para representar números com precisão total, seja em formatos inteiros ou decimais.  
Essa categoria inclui:
- **BIT**: usado para armazenar valores booleanos.
- **TINYINT, SMALLINT, INT, BIGINT**: inteiros de variados intervalos de tamanho.
- **NUMERIC / DECIMAL**: números decimais fixos com precisão total.
- **MONEY / SMALLMONEY**: usados para valores monetários com exatidão.

Esses tipos são projetados para facilitar operações financeiras, garantindo precisão nos cálculos e armazenamento eficiente. Money Smallmoney



O SQL fornece vários tipos de dados para trabalhar com strings, que são sequências de caracteres. Esses tipos permitem armazenar, manipular e recuperar dados textuais de maneira estruturada.

- **CHAR(n)** → Comprimento fixo. Exemplo: códigos como CPF, CEP.  
- **VARCHAR(n)** → Comprimento variável. Exemplo: nomes, endereços.  
- **TEXT / VARCHAR(MAX)** → Grandes blocos de texto. Exemplo: observações, descrições longas.  

### Quando usar?
1. **Armazenar dados textuais** → nomes, descrições, endereços.  
2. **Definir tipos de dados de coluna** → especificar quais dados podem ser armazenados.  
3. **Controlar tamanho dos dados** → limitar quantidade de texto com CHAR ou VARCHAR.
   
# Tipos de Dados em SQL

## Tipos Numéricos Exatos

| Tipo de Dado   | Valor Mínimo                              | Valor Máximo                              | Tamanho (em bytes) |
|----------------|--------------------------------------------|--------------------------------------------|---------------------|
| **bit**        | 0                                          | 1                                          | 1/8                 |
| **tinyint**    | 0                                          | 255                                        | 1                   |
| **smallint**   | -32,768                                    | 32,767                                     | 2                   |
| **int**        | -2,147,483,648                             | 2,147,483,647                              | 4                   |
| **bigint**     | -9,223,372,036,854,775,808                 | 9,223,372,036,854,775,807                  | 8                   |
| **decimal(p,s)** | Varia com precisão e escala               | Varia com precisão e escala                 | 5-17                |
| **numeric(p,s)** | Varia com precisão e escala               | Varia com precisão e escala                 | 5-17                |
| **money**      | -922,337,203,685,477.5808                  | 922,337,203,685,477.5807                   | 8                   |
| **smallmoney** | -214,748.3648                              | 214,748.3647                               | 4                   |

---

## Tipos Numéricos Aproximados

Para representações numéricas que não requerem precisão absoluta, o SQL Server oferece tipos numéricos aproximados, como **float** e **real**.  
Esses tipos são ideais para armazenar números em formatos científicos ou quando trabalhamos com grandes intervalos de valores, onde uma aproximação é aceitável.

| Tipo   | Valor Mínimo | Valor Máximo | Tamanho (em bytes) | Precisão     |
|--------|--------------|--------------|---------------------|--------------|
| **float** | -1.79E+308 | 1.79E+308    | 4 ou 8              | Depende de n |
| **real**  | -3.40E+38  | 3.40E+38     | 4                   | 7 dígitos    |

---

## Tipos de String

O SQL fornece vários tipos de dados para trabalhar com strings, que são sequências de caracteres. Esses tipos de dados permitem armazenar, manipular e recuperar dados textuais de maneira estruturada.

- **CHAR(n)** → comprimento fixo.  
- **VARCHAR(n)** → comprimento variável.  
- **TEXT / VARCHAR(MAX)** → grandes blocos de texto.  

### Quando usar?

1. **Armazenar dados textuais**: nomes, descrições, endereços, etc.  
2. **Definir tipos de dados de coluna**: especificar quais dados podem ser armazenados em uma coluna ao criar tabelas.  
3. **Controlar tamanho dos dados**: usar **CHAR** para tamanho fixo e **VARCHAR** para tamanho variável.


# Tipos de Dados em SQL

## Tipos Numéricos Exatos

| Tipo de Dado   | Valor Mínimo                              | Valor Máximo                              | Tamanho (em bytes) |
|----------------|--------------------------------------------|--------------------------------------------|---------------------|
| **bit**        | 0                                          | 1                                          | 1/8                 |
| **tinyint**    | 0                                          | 255                                        | 1                   |
| **smallint**   | -32,768                                    | 32,767                                     | 2                   |
| **int**        | -2,147,483,648                             | 2,147,483,647                              | 4                   |
| **bigint**     | -9,223,372,036,854,775,808                 | 9,223,372,036,854,775,807                  | 8                   |
| **decimal(p,s)** | Varia com precisão e escala               | Varia com precisão e escala                 | 5-17                |
| **numeric(p,s)** | Varia com precisão e escala               | Varia com precisão e escala                 | 5-17                |
| **money**      | -922,337,203,685,477.5808                  | 922,337,203,685,477.5807                   | 8                   |
| **smallmoney** | -214,748.3648                              | 214,748.3647                               | 4                   |

---

## Tipos Numéricos Aproximados

Para representações numéricas que não requerem precisão absoluta, o SQL Server oferece tipos numéricos aproximados, como **float** e **real**.  
Esses tipos são ideais para armazenar números em formatos científicos ou quando trabalhamos com grandes intervalos de valores, onde uma aproximação é aceitável.

| Tipo   | Valor Mínimo | Valor Máximo | Tamanho (em bytes) | Precisão     |
|--------|--------------|--------------|---------------------|--------------|
| **float** | -1.79E+308 | 1.79E+308    | 4 ou 8              | Depende de n |
| **real**  | -3.40E+38  | 3.40E+38     | 4                   | 7 dígitos    |

---

## Tipos de String

O SQL fornece vários tipos de dados para trabalhar com strings, que são sequências de caracteres. Esses tipos de dados permitem armazenar, manipular e recuperar dados textuais de maneira estruturada.

- **CHAR(n)** → comprimento fixo.  
- **VARCHAR(n)** → comprimento variável.  
- **TEXT / VARCHAR(MAX)** → grandes blocos de texto.  

### Quando usar?

1. **Armazenar dados textuais**: nomes, descrições, endereços, etc.  
2. **Definir tipos de dados de coluna**: especificar quais dados podem ser armazenados em uma coluna ao criar tabelas.  
3. **Controlar tamanho dos dados**: usar **CHAR** para tamanho fixo e **VARCHAR** para tamanho variável.
4. 
# Tipos de Dados de String em SQL

Os tipos de dados de string permitem armazenar e manipular informações textuais dentro de tabelas de banco de dados.  

---

## Funcionalidades Principais
4. **Integridade dos dados**: aplicar restrições como limites de comprimento e conjuntos de caracteres.  
5. **Pesquisar e manipular texto**: operações como localizar palavras ou caracteres dentro de uma string.  
6. **Classificar e comparar**: ordenar nomes em ordem alfabética ou comparar strings.  

---

## Sintaxe Básica
```sql
Column_name data_type(size);
```

- **column_name**: o nome da coluna onde os dados da string serão armazenados.  
- **data_type**: o tipo de dado de string (por exemplo, CHAR, VARCHAR, TEXT).  
- **size**: o comprimento máximo em caracteres da string (opcional para alguns tipos).  

---

## Valores de Parâmetros

- **column_name**: escolha nomes descritivos.  
- **data_type**: selecione o tipo apropriado:  
  - **CHAR(size)** → comprimento fixo.  
  - **VARCHAR(size)** → comprimento variável.  
  - **TEXT** → sequências de texto de tamanho variável.  
- **size**: define o comprimento máximo da string.  

---

## Exemplo Prático

A tabela `funcionarios` terá uma coluna para armazenar nomes de até 50 caracteres:  

```sql
CREATE TABLE funcionarios (
    id INT PRIMARY KEY,
    nome VARCHAR(50) NOT NULL
);
```

---

# Tipos de Dados de Data e Hora em SQL (MySQL)

Os tipos de dados de **data e hora** permitem armazenar valores temporais como datas, horas e anos.  
No MySQL, os principais tipos são: **DATE, TIME, DATETIME, TIMESTAMP, YEAR**.

---


### Dados Exemplo
| employee_id | employee_name   | hire_date   | last_login           |
|-------------|-----------------|-------------|----------------------|
| 1           | John Doe        | 2020-05-10  | 2025-10-08 12:30:45 |
| 2           | Jane Smith      | 2021-02-15  | 2025-10-08 12:30:45 |
| 3           | Michael Johnson | 2019-09-01  | 2025-10-08 12:30:45 |

---

## Considerações Gerais
- O MySQL **recupera valores em formato padrão**, mas interpreta várias formas de entrada.  
- Datas devem estar sempre no formato **ano-mês-dia** (`YYYY-MM-DD`).  
- Para converter formatos diferentes, pode-se usar `STR_TO_DATE()`.  
- Valores de **ano com dois dígitos** são interpretados assim:  
  - `70-99` → 1970-1999  
  - `00-69` → 2000-2069  
- Valores inválidos são transformados em **datas “zero”** (`0000-00-00`) por padrão.  
- O modo `ALLOW_INVALID_DATES` permite armazenar datas possivelmente incorretas (ex.: `2009-11-31`).  
- O modo `NO_ZERO_IN_DATE` impede meses/dias iguais a zero.  
- O modo `NO_ZERO_DATE` impede datas “fictícias” como `0000-00-00`.  

## Valores "Zero" Especiais

| Tipo de Dados | Valor “Zero”           |
|---------------|-------------------------|
| **DATE**      | `'0000-00-00'`          |
| **TIME**      | `'00:00:00'`            |
| **DATETIME**  | `'0000-00-00 00:00:00'` |
| **TIMESTAMP** | `'0000-00-00 00:00:00'` |
| **YEAR**      | `0000`                  |


# Regras e Restrições de Integridade em SQL

A **integridade de dados** se refere à acurácia, completude e consistência dos dados armazenados em um sistema de banco de dados.  
Isso garante que os dados possam ser armazenados, consultados e utilizados com confiabilidade.

As **restrições de integridade** ajudam a manter a precisão e consistência dos dados.  
Exemplos práticos:
- Em um banco de dados hospitalar, as alergias dos pacientes não podem ser deixadas em branco.
- Em um sistema financeiro, os valores das transações devem ser números positivos.

Em SQL, as restrições de integridade:
- Evitam a falta de dados.  
- Garantem que todos os dados estejam de acordo com os tipos e intervalos esperados.  
- Mantêm links adequados entre os dados de diferentes tabelas.  

---

## 🔑 Integridade da Entidade

A **integridade de entidade** garante que cada linha em uma tabela possa ser identificada de forma única.  
É implementada usando **Primary Keys (PK)** ou **Unique**.  

### Exemplo:

| id_cliente (PK) | nome | telefone      |
|-----------------|------|--------------|
| 1               | Ana  | (99)99999-9999 |
| 2               | João | (99)99999-9999 |

➡ O campo `id_cliente` é a **chave primária** e garante que não existam valores duplicados ou nulos.

### Regra:
- Nenhuma chave primária (PK) pode ser `NULL`.  
- Cada registro deve ter um identificador único.

---

## 🔗 Integridade Referencial

A **integridade referencial** mantém a consistência entre tabelas relacionadas por **chaves estrangeiras (FK)**.  
Ela garante que um valor em uma tabela corresponda a um valor existente em outra, evitando dados "órfãos".

### Exemplo:

**Tabela CLIENTE**  
| id_cliente (PK) | nome |
|-----------------|------|
| 1               | Ana  |
| 2               | João |

**Tabela PEDIDO**  
| id_pedido (PK) | id_cliente (FK) | valor  |
|----------------|-----------------|--------|
| 5001           | 1               | 120,00 |
| 5002           | 2               | 340,00 |

➡ O campo `id_cliente` em **PEDIDO** é uma chave estrangeira (FK).  
Ele só pode conter valores que existam na tabela **CLIENTE**.  
Não é permitido cadastrar um pedido com `id_cliente = 3`, se esse cliente não existir.

# Regras e Restrições de Integridade em SQL (Parte 2)

## Restrições de Integridade Referencial
A **Integridade Referencial** é utilizada entre duas relações e garante a consistência entre tuplas de tabelas diferentes. 
Ela afirma que uma tupla em uma relação que referencia outra precisa se referir a uma tupla **existente** nessa relação.

Essa restrição garante o vínculo entre duas tabelas usando **chaves primárias (PK)** ou **chaves alternativas (UNIQUE)** que são referenciadas em outra tabela como **chaves estrangeiras (FK)**.

Se o valor de uma chave estrangeira não existir na tabela de referência, pode ser preenchido com **NULL**, para manter a integridade.

---

## Integridade da Chave
A **Integridade da Chave** assegura que os valores usados como chaves em um banco de dados sejam precisos e consistentes, evitando inconsistências e registros órfãos.

As principais restrições de integridade em SQL incluem:

- **PRIMARY KEY**: Identifica de forma exclusiva cada registro em uma tabela.  
- **NOT NULL**: Impede que uma coluna aceite valores nulos.  
- **UNIQUE**: Garante que os valores de uma coluna ou grupo de colunas não se repitam.  
- **DEFAULT**: Define um valor padrão para uma coluna.  
- **CHECK**: Impõe uma condição que os valores de uma coluna devem atender.  
- **FOREIGN KEY**: Cria relacionamentos entre tabelas.

---

## Caso de Estudo: Banco de Dados Universitário

### Tabela `students`
- **student_id**: Identificador do aluno (PK).  
- **first_name**: Primeiro nome.  
- **last_name**: Sobrenome.  
- **email**: Endereço de e-mail.  
- **major**: Curso do aluno.  
- **enrollment_year**: Ano de matrícula.  

### Tabela `courses`
- **course_id**: Identificador do curso (PK).  
- **course_name**: Nome do curso.  
- **department**: Departamento responsável.  

### Tabela `enrollments`
- **student_id**: Identificador do aluno (FK referenciando `students`).  
- **course_id**: Identificador do curso (FK referenciando `courses`).  
- **year**: Ano da matrícula.  
- **grade**: Nota do aluno.  

# Restrições de Chaves em SQL

## Restrições da Chave Primária (PRIMARY KEY)
- Uma tabela geralmente possui uma coluna ou uma combinação de colunas que identifica de forma **única** cada linha.  
- Essa coluna (ou conjunto de colunas) é chamada de **chave primária (PK)**.  
- A **PRIMARY KEY** garante a **integridade da entidade**.  
- O banco de dados cria automaticamente um **índice exclusivo** para a PK, otimizando o acesso e consultas.  
- Se uma chave primária for definida em mais de uma coluna (**chave composta**), os valores podem se repetir em colunas individuais, mas **a combinação deve ser única**.

### Exemplo em SQL
```sql
CREATE TABLE clientes (
    id_cliente INT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    telefone VARCHAR(20)
);
```

---

## Restrições da Chave Estrangeira (FOREIGN KEY)
- Uma **FOREIGN KEY (FK)** é usada para criar vínculos entre tabelas.  
- Ela garante que o valor em uma coluna da tabela de referência corresponda a um valor existente na **PRIMARY KEY** de outra tabela.  
- Isso assegura **integridade referencial** entre tabelas.  

### Exemplo em SQL
```sql
CREATE TABLE pedidos (
    id_pedido INT PRIMARY KEY,
    id_cliente INT,
    valor DECIMAL(10,2),
    FOREIGN KEY (id_cliente) REFERENCES clientes(id_cliente)
);
```

Neste exemplo, `id_cliente` em `pedidos` só pode conter valores que já existam em `clientes`.

---

## Restrições de Integridade de Chave
Além das **PKs e FKs**, existem também **chaves candidatas** e a cláusula **UNIQUE**:

- **PRIMARY KEY** → identificador único para cada tupla.  
- **Candidatas** → colunas que poderiam ser chave primária, mas apenas uma é escolhida.  
- **UNIQUE** → usada para garantir que um atributo não se repita, mesmo que não seja a PK.  

### Exemplo com UNIQUE
```sql
CREATE TABLE usuarios (
    id_usuario INT PRIMARY KEY,
    email VARCHAR(150) UNIQUE,
    nome VARCHAR(100) NOT NULL
);
```

Nesse caso, mesmo que `email` não seja chave primária, ele não pode se repetir na tabela.

---




