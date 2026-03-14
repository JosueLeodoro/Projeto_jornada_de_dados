# 🚀 Projeto Jornada de Dados – Imersão Completa

## 📋 Sobre o Projeto

Este repositório documenta meu projeto prático desenvolvido durante a **Imersão Jornada de Dados**, uma experiência intensiva de 4 dias focada na construção de um pipeline completo de dados aplicado a um cenário real de e-commerce.

Durante a imersão, foi desenvolvido um fluxo completo de dados que inclui:

* Coleta e ingestão de dados
* Modelagem e estruturação em banco de dados
* Análise exploratória
* Engenharia e transformação de dados
* Uso de IA para desenvolvimento assistido

O projeto simula um ambiente real de negócio, onde uma empresa de **e-commerce** utiliza dados para melhorar decisões estratégicas.

---

# 🎯 Objetivo do Projeto

Construir uma arquitetura de dados capaz de:

* 📊 Analisar vendas e comportamento de clientes
* 🏪 Comparar preços com concorrentes
* 📈 Gerar métricas de negócio
* 🤖 Utilizar inteligência artificial para auxiliar no desenvolvimento e análise de dados

---

# 🧠 Tecnologias Utilizadas

* Python
* SQL
* Pandas
* dbt
* Supabase
* Amazon S3
* Antigravity IDE
* IA Assistida (Gemini e Claude)

---

# 📚 Estrutura da Imersão (4 Dias)

## 📊 Dia 1 — SQL, Banco de Dados e Modelagem

Primeiro contato com os dados e estruturação da base analítica.

Atividades realizadas:

* Criação do banco de dados utilizando **Supabase**
* Modelagem das tabelas do sistema
* Importação dos datasets
* Escrita de consultas SQL para análise de negócio
* Estruturação do esquema relacional

Objetivos do dia:

* Identificar produtos mais vendidos
* Analisar clientes
* Calcular métricas de vendas
* Explorar dados de concorrentes

Principais conceitos aplicados:

* Joins
* Agregações
* CASE WHEN
* GROUP BY
* Análise de métricas de negócio

---

## 🐍 Dia 2 — Análise Exploratória de Dados (EDA)

Neste dia os dados foram analisados utilizando **Python e Pandas**.

Atividades realizadas:

* Leitura dos datasets
* Limpeza e tratamento de dados
* Criação de métricas analíticas
* Visualização e exploração estatística
* Integração do pipeline com armazenamento em **Amazon S3**
* Sincronização dos dados com o banco do **Supabase**

Ferramentas utilizadas:

* Pandas
* Python
* Supabase
* Amazon S3

Objetivo:

Entender padrões de comportamento nos dados antes da modelagem analítica.

---

## ⚙️ Dia 3 — Engenharia de Dados com dbt

Neste dia o foco foi transformar scripts em um pipeline estruturado.

Atividades realizadas:

* Uso da **IDE Antigravity**
* Desenvolvimento assistido por **Gemini**
* Implementação de modelos analíticos com **dbt**
* Transformação e padronização de dados
* Sincronização e manutenção do banco de dados no **Supabase**

Conceitos aplicados:

* Data Modeling
* Transformações com dbt
* Camadas de dados
* Versionamento de modelos

Objetivo:

Criar uma estrutura escalável de dados pronta para análises e consumo.

---

## 🤖 Dia 4 — IA Aplicada ao Desenvolvimento

O último dia foi focado no uso de IA para acelerar o desenvolvimento.

Atividades realizadas:

* Utilização da **Antigravity IDE**
* Desenvolvimento assistido com **Claude**
* Geração de insights a partir dos dados
* Automação de tarefas de análise

Objetivo:

Explorar como ferramentas de **IA podem aumentar a produtividade em projetos de dados**.

---

# 🎲 Datasets Utilizados

O projeto utiliza **datasets sintéticos gerados com Faker**, simulando dados reais de um e-commerce.

Arquivos utilizados:

* `produtos.csv` → catálogo de produtos
* `clientes.csv` → base de clientes
* `vendas.csv` → histórico de vendas
* `preco_competidores.csv` → preços de concorrentes

## Arquivos utilizados estão na pasta data ##

Características dos dados:

* Distribuições realistas
* Relacionamentos entre tabelas
* Dados com inconsistências para prática de limpeza
* Cenário realista de mercado

---

# 📊 Estrutura dos Dados

### Produtos

```
id_produto
nome_produto
categoria
marca
preco_atual
data_criacao
```

### Clientes

```
id_cliente
nome_cliente
estado
pais
data_cadastro
```

### Vendas

```
id_venda
data_venda
id_cliente
id_produto
canal_venda
quantidade
preco_unitario
```

### Preços de Concorrentes

```
id_produto
nome_concorrente
preco_concorrente
data_coleta
```

---

# 🔗 Relacionamento entre Tabelas

```
clientes
   │
   │
   ▼
vendas
   ▲
   │
produtos
   │
   ▼
preco_competidores
```

---

# 📊 Perguntas de Negócio Respondidas

Durante o projeto foram analisadas diversas perguntas estratégicas, como:

* Quais são os produtos mais vendidos?
* Quais clientes geram maior receita?
* Qual o ticket médio por cliente?
* Quais produtos estão mais caros que os concorrentes?
* Qual categoria gera mais receita?
* Quais produtos nunca foram vendidos?

---

# 📂 Estrutura do Repositório

```
Projeto-Jornada-De-Dados/

data/
produtos.csv
clientes.csv
vendas.csv
preco_competidores.csv

generate_datasets.py

aulas/
aula-01-sql/
aula-02-python/
aula-03-engenharia/
aula-04-ia/

README.md
```

---

# 🚀 Como Executar o Projeto

Instale as dependências:

```bash
pip install faker pandas
```

Gere os datasets:

```bash
python generate_datasets.py
```

Os arquivos serão gerados na pasta `data/`.

---

# 🎯 Resultados da Imersão

Ao final do projeto foi possível desenvolver:

✔ Estrutura completa de banco de dados
✔ Pipeline de ingestão e transformação de dados
✔ Análise exploratória com Python
✔ Modelagem analítica com dbt
✔ Integração com Supabase e S3
✔ Uso de IA para desenvolvimento assistido

---

# 💡 Aprendizados

Este projeto reforçou conceitos importantes da área de dados:

* Pensamento analítico orientado a negócio
* Construção de pipelines de dados
* Modelagem e transformação de dados
* Uso de IA como ferramenta de produtividade

---

# 📌 Sobre o Autor

Projeto desenvolvido por **Josué Costa** durante a Imersão Jornada de Dados.

Interesses principais:

* Data Analytics
* Data Science
* Engenharia de Dados
* Inteligência Artificial aplicada a dados

---

⭐ Caso este projeto seja útil para você, considere dar uma **star no repositório**.
