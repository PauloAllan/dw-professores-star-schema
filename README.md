# 🌟 Desafio de Modelagem Dimensional: Star Schema (DW Professores)

Projeto de desenvolvimento e implementação de um **Data Warehouse em Modelo Estrela (Star Schema)** utilizando MySQL. O objetivo é transformar um modelo relacional OLTP em um modelo multidimensional OLAP para suportar análises de dados e inteligência de negócios (BI).

---

## 🎯 Escopo do Desafio
O objetivo principal é reestruturar as entidades acadêmicas para permitir a análise de indicadores como **quantidade de ofertas de disciplinas** e **carga horária total**, segmentados por professor, departamento, curso, disciplina e tempo.

---

## 📐 Estrutura do Star Schema

O modelo é composto por **1 Tabela Fato Central** e **5 Tabelas de Dimensão**:

### 📊 Tabela Fato
* **`fato_ensino`**: Centraliza os eventos de oferta de disciplinas. Contém as métricas numéricas (`quantidade_ofertas`, `carga_horaria_total`) e as chaves estrangeiras (`FKs`) que conectam às dimensões.

### 🏷️ Tabelas de Dimensão
* **`dim_professor`**: Armazena atributos dos docentes (nome, titulação, situação).
* **`dim_departamento`**: Informações administrativas (nome do departamento e sigla).
* **`dim_curso`**: Dados dos cursos oferecidos (nome, nível e modalidade).
* **`dim_disciplina`**: Especificações técnicas das disciplinas (código e carga horária).
* **`dim_data`**: Granularidade temporal (chave `YYYYMMDD`, dia, mês, trimestre, ano) para permitir análise de séries temporais.

---

## 🖼️ Diagrama de Relacionamento (ER)

O diagrama abaixo ilustra a arquitetura **Star Schema** gerada no DBeaver, onde a tabela fato se conecta diretamente às 5 dimensões (relacionamento 1:N):

![Diagrama ER Star Schema](./diagrama_er.png)

---

## 🛠️ Tecnologias Utilizadas
* **SGBD:** MySQL Server 8.0+
* **SQL Editor:** DBeaver / MySQL Workbench
* **Linguagem:** SQL (DDL e DML)

---

## 🚀 Como Executar o Projetos

1. Clone este repositório:
   ```bash
   git clone [https://github.com/PauloAllan/dw-professores-star-schema.git](https://github.com/PauloAllan/dw-professores-star-schema.git)
