Este projeto consiste na construção de um mini pipeline de ETL (Extract, Transform, Load) utilizando Python, SQLite e SQL, com o objetivo de realizar o tratamento e a transformação de dados de pacientes com diabetes, gerando um novo dataset pronto para análise.

O processo envolve a leitura de um arquivo CSV, armazenamento dos dados em um banco de dados relacional SQLite, aplicação de filtros e regras de negócio e, por fim, a exportação dos dados processados para um novo arquivo CSV.

---

## 🎯 Objetivo

Gerar uma amostra de dados contendo apenas pacientes com mais de 50 anos e classificar cada paciente como:

* **Normal** → IMC (BMI) menor que 30
* **Obeso** → IMC maior ou igual a 30

O resultado final é salvo em um arquivo CSV para posterior análise por cientistas de dados.

---

## 🧠 Etapas do Processo (ETL)

### 1. Extração

* Leitura do arquivo `diabetes.csv` usando Pandas.
* Importação dos dados para uma tabela SQLite chamada `diabetes`.

### 2. Transformação

* Criação de uma nova tabela `pacientes` contendo apenas registros com idade superior a 50 anos.
* Adição da coluna `perfil` para classificar os pacientes com base no valor do BMI.
* Atualização dos registros conforme regra de negócio.

### 3. Carga

* Conversão dos dados finais em um DataFrame.
* Exportação do resultado para o arquivo `pacientes.csv`.

---

## 🛠️ Tecnologias Utilizadas

* Python 3
* SQLite
* SQL
* Pandas
* Jupyter Notebook

---

## 📂 Estrutura do Projeto

```bash
etl-diabetes-sqlite-python/
│
├── dataset/
│   ├── diabetes.csv
│   └── pacientes.csv
│
├── database/
│   └── dbprojeto1.db
│
├── notebook.ipynb
└── README.md
```

---

## 🔄 Fluxo Simplificado

```
Arquivo CSV → SQLite → Filtro + Classificação → DataFrame → CSV Final
```

---

## 📈 Resultado Final

O projeto gera um arquivo chamado `pacientes.csv` contendo os seguintes campos:

* Pregnancies
* Glucose
* BloodPressure
* SkinThickness
* Insulin
* BMI
* DiabetesPedigreeFunction
* Age
* Outcome
* perfil (Normal ou Obeso)

Pronto para ser utilizado em análises, dashboards ou modelos preditivos.

---

## ✅ Aprendizados

Durante o desenvolvimento deste projeto foram aplicados conceitos como:

* Manipulação de dados com Pandas
* Operações SQL básicas
* Criação e manipulação de banco de dados SQLite
* Conceito prático de ETL
* Integração entre Python e SQL

---

## 🚀 Como executar o projeto

1. Instale as dependências:

```bash
pip install pandas sqlite3 ipython-sql watermark
```

2. Execute o notebook:
   Abra o arquivo `.ipynb` no Jupyter Notebook e execute as células em ordem.

---

## 👤 Autor

**Ivaldo Neto**
Estudante e entusiasta de Dados e Tecnologia

---
