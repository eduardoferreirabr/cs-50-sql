# CS50's Introduction to Databases with SQL 🎓

Repositório dedicado aos estudos, anotações e resoluções práticas do curso **[CS50's Introduction to Databases with SQL](https://cs50.harvard.edu/sql/)**, oferecido pela **Universidade de Harvard** através do *OpenCourseWare* e *edX*, ministrado pelos professores **Carter Zenke** e **David J. Malan**.

---

## 📌 Sobre o Curso

O **CS50 SQL** é uma introdução completa ao universo dos bancos de dados relacionais e à linguagem **SQL** (*Structured Query Language*). O curso aborda desde a criação, consulta, atualização e exclusão de dados (**CRUD**), até modelagem avançada de entidades, normalização, integridade referencial, otimização com índices, transações (**ACID**) e conceitos de escalabilidade com sistemas cliente-servidor como **PostgreSQL** e **MySQL**.

### Principais Habilidades Desenvolvidas:
- **Modelagem Relacional:** Criação de tabelas, tipos de dados, chaves primárias (*Primary Keys*), chaves estrangeiras (*Foreign Keys*), restrições (*Constraints*) e gatilhos (*Triggers*).
- **Consultas e Relacionamentos:** Filtros, funções de agregação, ordenação, subqueries, uniões e junções (*INNER, LEFT, RIGHT, FULL JOINs*).
- **Normalização de Dados:** Eliminação de redundâncias e garantia de integridade até a Terceira Forma Normal (3NF).
- **Visões e Abstração:** Criação de *Views*, visões temporárias e Expressões de Tabela Comuns (*Common Table Expressions - CTEs*).
- **Otimização e Concorrência:** Criação e análise de índices (*B-Trees*), planos de execução (`EXPLAIN QUERY PLAN`), transações e propriedades ACID.
- **Escala e Integração:** Diferenças de tipagem e arquitetura entre SQLite, MySQL e PostgreSQL, além da integração de bancos de dados com linguagens como Python e Java.

---

## 📚 Ementa e Conteúdo Programático

| Semana | Tópico | Principais Conceitos | Problem Set (Projetos Práticos) |
| :---: | :--- | :--- | :--- |
| **0** | **[Querying](https://cs50.harvard.edu/sql/weeks/0/)** | `SELECT`, `WHERE`, `LIMIT`, `OFFSET`, `ORDER BY`, `LIKE`, `NULL`, operadores lógicos e funções de agregação (`COUNT`, `AVG`, `SUM`, `MIN`, `MAX`). | • *Cyberchase*<br>• *36 Views* ou *Normals*<br>• *Players* |
| **1** | **[Relating](https://cs50.harvard.edu/sql/weeks/1/)** | Diagramas Entidade-Relacionamento (ERD), Chaves Primárias/Estrangeiras, Subconsultas (*Subqueries*), `JOIN`s, Operações de Conjunto (`UNION`, `INTERSECT`, `EXCEPT`), `GROUP BY`, `HAVING`. | • *Packages, Please*<br>• *DESE*<br>• *Moneyball* |
| **2** | **[Designing](https://cs50.harvard.edu/sql/weeks/2/)** | *Schemas*, Normalização de dados (1NF, 2NF, 3NF), Tipos de dados, Afinidades de tipos, Restrições de tabela e coluna (`CHECK`, `DEFAULT`, `UNIQUE`, `NOT NULL`), `ALTER TABLE`. | • *ATL*<br>• *Happy to Connect*<br>• *Union Square Donuts* |
| **3** | **[Writing](https://cs50.harvard.edu/sql/weeks/3/)** | Operações CRUD: `INSERT INTO`, importação de CSVs (`.import`), `UPDATE`, `DELETE FROM`, exclusão em cascata, *Triggers* e exclusões lógicas (*Soft Deletions*). | • *Don’t Panic!*<br>• *Meteorite Cleaning* |
| **4** | **[Viewing](https://cs50.harvard.edu/sql/weeks/4/)** | *Views*, *Temporary Views*, CTEs (*Common Table Expressions*), particionamento lógico e segurança de acesso aos dados. | • *Census Taker*<br>• *The Private Eye*<br>• *Bed and Breakfast* |
| **5** | **[Optimizing](https://cs50.harvard.edu/sql/weeks/5/)** | Índices (`CREATE INDEX`), *Covering Indexes*, *Partial Indexes*, Árvores B (*B-Trees*), `EXPLAIN QUERY PLAN`, `VACUUM`, Concorrência, Transações e propriedades ACID. | • *In a Snap*<br>• *your.harvard* |
| **6** | **[Scaling](https://cs50.harvard.edu/sql/weeks/6/)** | Escalabilidade, arquitetura cliente-servidor, introdução ao MySQL e PostgreSQL, *Stored Procedures*, autenticação, conexão com Python e Java. | • *Happy to Connect (Sentimental)*<br>• *From the Deep*<br>• *Don’t Panic! (Python/Java)* |
| **Final** | **[Final Project](https://cs50.harvard.edu/sql/project/)** | Projeto final: especificação, modelagem de esquema, diagrama ER, implementação de banco de dados relacional e consultas representativas. | Projeto autoral completo |

---

## 📂 Estrutura do Repositório

O repositório está organizado modularmente por aulas e exercícios práticos em `src/cs_50_sql/`:

```text
cs-50-sql/
├── README.md
├── src/
│   └── cs_50_sql/
│       └── aulas/
│           ├── aula_00/                                  # Week 0: Querying
│           │   ├── CS50 SQL - Lecture 0 - Querying.md    # Notas e resumo teórico da aula
│           │   └── source_code/                          # Códigos e banco de dados da aula
│           │       ├── 00_SELECT.sql
│           │       ├── 01_LIMIT.sql
│           │       ├── 03_WHERE.sql
│           │       ├── 04_compound.sql
│           │       ├── 05_NULL.sql
│           │       ├── 06_LIKE.sql
│           │       ├── 07_range.sql
│           │       ├── 08_ORDER BY.sql
│           │       ├── 09_aggregate.sql
│           │       └── longlist.db                       # Banco de dados de exemplo
│           ├── aula_01/                                  # Week 1: Relating
│           │   ├── CS50 SQL - Lecture 1 - Relating.md    # Notas da aula e diagramas ER
│           │   └── source_code/
│           │       ├── groups.sql
│           │       ├── joins.sql
│           │       ├── nested.sql
│           │       ├── sets.sql
│           │       ├── longlist.db
│           │       └── sea_lions.db
│           └── ...                                       # Próximas semanas (em andamento)
```

---

## 🛠️ Tecnologias e Ferramentas

- **[SQLite](https://www.sqlite.org/):** RDBMS leve e baseado em arquivo utilizado nas semanas iniciais.
- **[PostgreSQL](https://www.postgresql.org/) & [MySQL](https://www.mysql.com/):** SGBDs cliente-servidor utilizados nas etapas avançadas e de escala.
- **[Visual Studio Code](https://code.visualstudio.com/) / [CS50 Dev](https://cs50.dev/):** Ambiente de desenvolvimento e extensão *SQLite Viewer*.
- **[Mermaid.js](https://mermaid.js.org/):** Utilizado para renderização de diagramas ER diretamente na documentação Markdown.

---

## 🚀 Como Executar os Exemplos

### 1. Pré-requisitos
Certifique-se de ter o **SQLite 3** instalado em seu sistema operacional:
```bash
# No Ubuntu/Debian:
sudo apt update && sudo apt install sqlite3
```

### 2. Abrindo um banco de dados e executando scripts
Navegue até a pasta da aula desejada e inicie a CLI do SQLite com o banco correspondente:

```bash
cd "src/cs_50_sql/aulas/aula_00/source_code"
sqlite3 longlist.db
```

Dentro do prompt interativo do SQLite:
```sql
-- Exibir as tabelas existentes
.tables

-- Exibir o esquema da tabela
.schema books

-- Executar um arquivo SQL
.read 00_SELECT.sql

-- Formatar a saída de dados em colunas legíveis
.mode table
SELECT title, author FROM books LIMIT 5;

-- Sair do prompt
.quit
```

---

## 🔗 Links Úteis e Referências Oficiais

- 🌐 **Site Oficial do Curso:** [cs50.harvard.edu/sql](https://cs50.harvard.edu/sql/)
- 📖 **EdX Course:** [CS50's Introduction to Databases with SQL](https://cs50.edx.org/sql)
- 📺 **Playlist no YouTube:** [CS50 SQL Lectures](https://www.youtube.com/playlist?list=PLhQjrBD2T382v1MBjNOhPu9SiJ1fsD4C0)
- 🤖 **Assistente CS50.ai:** [cs50.ai](https://cs50.ai/)
- 💻 **Ambiente Web CS50 Dev:** [cs50.dev](https://cs50.dev/)
- 📜 **Licença:** Todo o material do curso é disponibilizado sob a [licença do CS50](https://cs50.harvard.edu/sql/license/).
