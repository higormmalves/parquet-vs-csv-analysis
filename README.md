# CSV vs Parquet: File Formats Comparison for Data Engineering

# [PT-BR]

## 📌 Objetivo

Este projeto foi desenvolvido como parte do meu roadmap de estudos em **Data Engineering**, com o objetivo de compreender diferentes formatos de armazenamento de dados e avaliar, na prática, as vantagens do formato **Parquet** em comparação ao formato **CSV**.

O experimento consiste em converter um dataset real em CSV para Parquet e comparar:

* Tamanho ocupado em disco;
* Tempo de escrita dos arquivos.

---

## 📚 Conceitos estudados

## CSV (Comma-Separated Values)

Formato de arquivo amplamente utilizado para troca de dados entre sistemas.

### Vantagens

* Fácil leitura por humanos;
* Alta compatibilidade entre ferramentas;
* Simples de criar e compartilhar.

### Limitações

* Não possui schema definido;
* Armazena dados como texto;
* Arquivos geralmente maiores;
* Menor eficiência para consultas analíticas em grandes volumes.

---

## JSON / JSONL

Formatos semi-estruturados utilizados principalmente em:

* APIs;
* Integrações entre sistemas;
* Streaming de dados.

### Características

* Alta flexibilidade;
* Suporte a estruturas aninhadas;
* Mais adequado para dados semi-estruturados.

Por outro lado, normalmente apresentam maior custo de armazenamento e menor eficiência para análises em larga escala.

---

## Parquet

Formato de armazenamento **colunar** desenvolvido para workloads analíticos.

### Principais vantagens

* Compressão eficiente;
* Armazena informações de schema;
* Melhor performance em consultas analíticas;
* Menor custo de armazenamento;
* Padrão utilizado em Data Lakes modernos.

Exemplo de arquitetura:

```
CSV
 |
 | ETL / ELT
 ↓
Parquet
 |
 ↓
Spark / Databricks / DuckDB / BigQuery
```

---

## Delta Lake / Apache Iceberg

Formatos construídos sobre Parquet que adicionam recursos de gerenciamento de dados, como:

* Transações ACID;
* Controle de versões;
* Evolução de schema;
* Time Travel;
* Arquitetura Lakehouse.

---

# 🛠️ Tecnologias utilizadas

* Python
* Pandas
* PyArrow

Instalação:

```bash
pip install pandas pyarrow
```

---

# 🔄 Processo realizado

Fluxo do experimento:

```
CSV
 |
 | Leitura utilizando Pandas
 |
 ↓
DataFrame
 |
 | Conversão utilizando PyArrow
 |
 ↓
Parquet
```

---

# 🧪 Implementação

O script realiza:

1. Leitura do arquivo CSV;
2. Conversão para Parquet;
3. Comparação do tamanho dos arquivos;
4. Comparação do tempo de escrita.

# 🎯 Aprendizados

Neste projeto foi possível compreender:

* Diferenças entre formatos estruturados e semi-estruturados;
* Limitações do CSV em ambientes analíticos;
* Funcionamento do armazenamento colunar;
* Conversão de arquivos utilizando Python;
* Impacto dos formatos de armazenamento em custo e eficiência.

---

# [EN]

## 📌 Objective

This project was developed as part of my **Data Engineering learning roadmap**, aiming to understand different data storage formats and evaluate the practical advantages of **Parquet** compared to **CSV**.

The experiment converts a real-world dataset from CSV to Parquet and compares:

* Disk storage size;
* File writing time.

---

## 📚 Concepts Studied

## CSV (Comma-Separated Values)

A widely used file format for data exchange between systems.

### Advantages

* Human-readable;
* High compatibility across tools;
* Simple to create and share.

### Limitations

* No defined schema;
* Stores data as plain text;
* Usually larger files;
* Less efficient for analytical workloads.

---

## JSON / JSONL

Semi-structured formats commonly used for:

* APIs;
* System integrations;
* Data streaming.

### Characteristics

* High flexibility;
* Supports nested structures;
* Suitable for semi-structured data.

However, they usually require more storage space and are less efficient for large-scale analytics.

---

## Parquet

A **columnar storage format** designed for analytical workloads.

### Main advantages

* Efficient compression;
* Schema preservation;
* Better analytical query performance;
* Lower storage costs;
* Widely adopted in modern Data Lakes.

Example architecture:

```
CSV
 |
 | ETL / ELT
 ↓
Parquet
 |
 ↓
Spark / Databricks / DuckDB / BigQuery
```

---

## Delta Lake / Apache Iceberg

Formats built on top of Parquet that provide additional data management capabilities:

* ACID transactions;
* Version control;
* Schema evolution;
* Time Travel;
* Lakehouse architecture.

---

# 🛠️ Technologies

* Python
* Pandas
* PyArrow

Installation:

```bash
pip install pandas pyarrow
```

---

# 🔄 Workflow

Experiment workflow:

```
CSV
 |
 | Read using Pandas
 |
 ↓
DataFrame
 |
 | Convert using PyArrow
 |
 ↓
Parquet
```

---

# 🧪 Implementation

The script performs:

1. CSV ingestion;
2. CSV to Parquet conversion;
3. File size comparison;
4. Write time comparison.

---

# 🎯 Key Learnings

This project helped me understand:

* Differences between structured and semi-structured formats;
* CSV limitations for analytical workloads;
* Columnar storage concepts;
* File conversion using Python;
* How storage formats impact efficiency and cost.

---
