Sobre o projeto

Este projeto tem como objetivo demonstrar a construção de um pipeline de dados bancário utilizando a arquitetura Medallion (Bronze, Silver e Gold) no Databricks, simulando um ambiente real de Engenharia de Dados.

Os dados foram gerados com a biblioteca Faker, representando as principais entidades de um banco:

Consumidores
Contas
Transações
Localizações

O pipeline foi desenvolvido seguindo boas práticas de Data Engineering, desde a ingestão até a disponibilização dos dados para consumo analítico por meio de dashboards.

Arquitetura
Bronze
Geração de dados fictícios utilizando Faker.
Ingestão realizada com PySpark.
Persistência dos dados em tabelas Delta Lake.
Silver
Transformações desenvolvidas em Databricks SQL.
Padronização dos dados.
Tratamento de inconsistências.
Aplicação de regras de qualidade.
Enriquecimento das informações.
Utilização de arquivos Parquet quando necessário para otimização do processamento.
Gold
Consolidação das tabelas da camada Silver.
Aplicação das regras de negócio.
Construção de tabelas analíticas para geração de indicadores e dashboards.
Orquestração

O pipeline foi orquestrado utilizando Databricks Workflows, garantindo a execução automática e controlada de todas as etapas do processamento.

Características da orquestração:

Execução paralela das cargas da camada Bronze.
Controle de dependências entre Bronze, Silver e Gold.
Execução sequencial da consolidação na camada Gold.
Validação automática após o processamento.
Configuração de retry para recuperação em caso de falhas.
Controle de concorrência do workflow.
Notificações por e-mail em caso de erro.
Dashboard

Após o processamento dos dados, foi desenvolvido um dashboard no Databricks SQL contendo indicadores como:

Total transacionado
Quantidade de transações
Ticket médio
Evolução mensal
Transações por tipo
Transações por canal
Transações por status
Tabela detalhada das transações
Tecnologias utilizadas
Databricks
PySpark
Databricks SQL
Delta Lake
Databricks Workflows
SQL Warehouse
Faker
Parquet
Objetivo

Demonstrar a implementação de um pipeline completo de Engenharia de Dados, desde a ingestão dos dados até sua disponibilização para análise, aplicando conceitos de arquitetura Lakehouse, orquestração, modelagem de dados e visualização de indicadores em um cenário bancário.

Essa descrição passa uma imagem muito profissional. Se um recrutador abrir seu GitHub e encontrar essa documentação, juntamente com o diagrama da arquitetura, o workflow do Databricks e o dashboard, verá um projeto bastante consistente e próximo de um ambiente corporativo.
