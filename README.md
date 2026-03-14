# 🛒 Projeto E-commerce com dbt - Engenharia de Dados

Bem-vindo(a) ao repositório do projeto de dados para **E-commerce**! 
Este projeto foi desenvolvido como parte do meu portfólio e estudos acadêmicos na área de **Dados (Engenharia e Analytics Engineering)**. Aqui, utilizo o **dbt (Data Build Tool)** para realizar a transformação de dados de um e-commerce fictício, preparando e modelando as informações desde a ingestão bruta até as métricas e KPIs prontas para consumo pelo negócio.

## 🎯 Objetivo do Projeto

O objetivo principal deste projeto é implementar e automatizar um pipeline de transformação de dados escalável utilizando as melhores práticas do mercado, em especial a **Arquitetura Medalhão (Medallion Architecture)**. Através desta abordagem, o projeto simula o tratamento de dados (como informações de clientes, vendas, produtos e concorrentes) a fim de fornecer insights rápidos, padronizados e de alta confiabilidade para analistas de BI e stakeholders.

## 🏗️ Arquitetura e Modelagem

O projeto é estruturado em três camadas (schemas) progressivas de qualidade de dados:

### 🥉 Camada Bronze (Raw)
- **Objetivo:** Ponto de entrada das fontes de dados (`sources`). Aqui, os dados estão em seu formato original, apenas espelhando a fonte física.
- **Materialização:** `view` (Visualizações leves e sem custo de storage que mantêm os dados sempre atualizados).
- **Modelos Integrados:** `bronze_clientes`, `bronze_produtos`, `bronze_vendas`, `bronze_preco_competidores`.

### 🥈 Camada Silver (Cleaned)
- **Objetivo:** Limpeza, padronização, tipagem forte e tratamento de anomalias. É aqui que joins estruturais começam a ser definidos e colunas calculadas de base são construídas.
- **Materialização:** `table` (Para garantir performance nas camadas seguintes).
- **Modelos Integrados:** `silver_clientes`, `silver_produtos`, `silver_vendas`, `silver_preco_competidores`.

### 🥇 Camada Gold (Business & KPIs)
- **Objetivo:** Camada de entrega de valor final ("Data Marts"), contendo as tabelas agregadas de negócio prontas para consumo em Dashboards (Power BI, Metabase, etc).
- **Materialização:** `table`
- **Domínios/Schemas:**
  - 🤝 **`customer_success`**: Foco na retenção, saúde e segmentação do cliente (ex: baseados na variável `segmentacao_vip_threshold` definida no projeto).
  - 💰 **`pricing`**: Comparações e otimizações de preço com relação a competidores.
  - 📊 **`sales`**: Métricas financeiras puras e desempenho comercial (LTV, Receita, Quantidades).

## 🛠️ Tecnologias e Ferramentas

- **dbt Core**: Ferramenta principal utilizada para orquestração das transformações (DAGs), execução de testes de qualidade, controle de versão e geração de documentação das tabelas.
- **SQL (Modelagem Dimensional)**: Transformação de dados, construção de fatos e dimensões (Star Schema).
- **Git** / **GitHub**: Versionamento de código.

## 🚀 Como Executar o Projeto Localmente

1. **Pré-requisitos**:
   Certifique-se de ter o [dbt (Data Build Tool)](https://docs.getdbt.com/) instalado com o adapter do seu Data Warehouse ativo (ex: BigQuery, Snowflake, PostgreSQL, etc).

2. **Configuração de Perfil (`profiles.yml`)**:
   Configure as credenciais e parâmetros de conexão de banco de dados no arquivo `~/.dbt/profiles.yml`, verificando se o nome do perfil de execução associado é `ecommerce`.

3. **Rodando os Modelos**:
   Para construir todos os modelos respeitando as dependências do projeto, execute o comando na raiz:
   ```bash
   dbt run
   ```

4. **Gerando e Analisando a Documentação**:
   Gere e inicie um servidor web local com a documentação do catálogo de dados:
   ```bash
   dbt docs generate
   dbt docs serve
   ```

## 👨‍💻 Sobre o Autor

Sou um estudante na área de Dados, apaixonado por explorar as novas ferramentas e arquiteturas do cenário moderno de engenharia e análise. Sinta-se à vontade para analisar o código, sugerir melhorias ou entrar em contato!
