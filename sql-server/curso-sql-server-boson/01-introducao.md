# Aula 00 - Intrudução

## Structured Query Language

- Linguagem de Consulta Estruturada padrão para acesso a Banco de Dados;
- Usada em inúmeros sistemas, como MySQL, SQL Server, Oracle, Sybase, Access, DB2, PostgreSQL, etc.
- Cada sistema pode usar um "dialeto" do SQL, como T-SQL (SQL Server), PL/SQL (Oracle), JET SQL (Access), etc.

## Funções do SQL

- Permite acesso a dados em SGBDR;
- Permite definir os dados no banco de dados e manipulá-los.
- Pode ser embutido em outras linguagens usando módulos SQL, bibliotecas, etc;
- Permite criar e excluir bancos de dados e tabelas;
- Permite a criação de Visões (Exibições), Stored Procedures e Funções em um Banco de Dados;
- Permite configurar permissões de acesso em tabelas, procedimentos e visões.

## Grupos de Comandos

Os comandos SQL podem ser divididos em quatro grupos principais:

- DDL
- DML
- DCL
- DQL

### DDL - Data Definition Language

| Comando | Descrição |
|---------|-----------|
| CREATE  | Cria uma nota tabela, visão ou outro objeto no DB. |
| ALTER   | Modifica um objeto existente no BD, como uma tabela. |
| DROP    | Exclui uma tabela inteira, uma exibição de uma tabela ou outro objeto no banco de dados. |

### DML - Data Manipulation Language

| Comando | Descrição |
|---------|-----------|
| INSERT  | Cria um registro (linha). |
| UPDATE  | Modifica registros. |
| DELETE  | Exclui registros. |

### DCL - Data Control Language

| Comando | Descrição |
|---------|-----------|
| GRANT   | Dá privilégios a um usuário. |
| REVOKE  | Retira privilégios fornecidos a um usuário. |

### DQL - Data Query Language

| Comando | Descrição |
|---------|-----------|
| SELECT   | Obtém registros especificados de uma ou mais tabelas. |

# Aula 01 - SGBDR

- Sistema Gerenciador de Banco de Dados Relacional
- Trata-se de um sistema de gerenciamento de bancos de dados baseado no modelo relacional introduzido por E.F.Codd.

## Banco de Dados Relacional

### Composição

- Tabelas
- Campos (Colunas)
- Registros (Linhas)

#### Tabelas

- Objetos onde são armazenados os dados de um banco de dados relacional.
- Uma tabela é uma coleção de entradas de dados relacionais e consiste em linhas e colunas.

#### Campo

- São entidades que representam os atributos dos dados, como Nome, Data de Nascimento, Salário, Preço, etc.
- Um campo é uma coluna em uma tabela que mantém informações específicas sobre cada registro.

#### Registro

- Linha, ou Tupla;
- Cada entrada individual em uma tabela. Trata-se de um conjunto de campos relacionados que caracterizam os dados de uma entidade única.

## Tipos de Dados SQLServer

| Tipo       | Descrição | Armazenamento |
|------------|-----------|---------------|
| char(n)    | String de caracteres de tamanho fixo, máximo de 8000 caracteres. | n |
| varchar(n) | String de caracteres de tamanho variável, máximo de 8000 caracteres. | |
| nchar(n)   | Dados Unicode de tamanho fixo, máximo de 4000 caracteres | |
| nvarchar(n) | Dados Unicode de tamanho fixo, máximo de 4000 caracteres. | |
| bit | 0, 1 ou nulo | |
| tinyint  | Números inteiros de 0 a 255 | 1 byte |
| smallint | Números inteiros de -32768 a 32767 | 2 bytes
| int      | Números inteiros entre -2,147,483,648 e 2,147,483,647 | 4 bytes | 
| bigint   | Números entre -9,223,372,036,854,775,808 e 9,223,372,036,854,775,807 | 8 bytes |
| real     | Números de ponto flutuante entre -3.4x10^38 e 3.4x10^38 | 4 bytes |
| datatime | De 01/01/1753 a 31/02/9999, com uma precisão de 3.33 milisegundos. | 8 bytes |
| smalldatatime | De 01/01/1900 a 06/06/2079, com precisão de 1 minuto. | 4 bytes |
| date    | Data apenas. De 01/01/0001 a 31/12/9999 | 3 bytes |
| time    | Hora apenas. Precisão de até 100 nanosegundos. | 3-5 bytes |
| text    | Cadeia de caracteres de tamanho variável. Até 2 GB de dados. | 
| money   | Dados monetários de -922,337,203,685,477.5808 até 922,337,203,685,477,5807 | 8 bytes |

# Aula 02 - Criação de um Banco de Dados

## Criando um Banco de dados

- Criando um novo banco de dados pela **interface**:
    - Clica com o esquerdo em cima de Bancos de dados e seleciona a opção **criar um novo banco de dados**:
        - Adicione nome e o proprietário.

- Criando via linha de comando:

```sql
CREATE DATABASE db_Biblioteca
ON PRIMARY (NAME=db_Biblioteca, 
FILENAME='C:\SQL\db_Biblioteca.MDF',
SIZE=10MB,
MAXSIZE=20MB,
FILEGROWTH=10%
)
```

Obs.: O SQLServer prefere aspas simples ('').

Banco DB Biblioteca que será utilizado no curso.

### Comentários

Para adicionar um comentário utilize o --:

```sql
--EXPLICAÇÃO OU COMANDO
```

## Comandos

### Comando USE

- O comando **USE** instrui o SGBDR a utilizar banco de dados especificado para rodar os comandos.
- Sintaxe:
``` sql
USE banco_de_dados
```

### Comando sp_helpdb

Informa o tamanho, taxa de crescimento, e local do banco de dados:
``` sql
sp_helpdb banco_de_dados
```

# CONSRRAINTS (Restrições) - PRIMARY KEY, NOT NULL, etc.













