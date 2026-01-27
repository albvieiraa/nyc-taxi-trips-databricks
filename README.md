# NYC Yellow Taxi — Analytics Project

Projeto de análise de dados utilizando SQL e Databricks, com foco em modelagem analítica, qualidade de dados e geração de KPIs de negócio a partir de dados públicos da NYC Taxi & Limousine Commission.

---

## 🎯 Objetivo do Projeto
- Praticar SQL analítico no Databricks
- Implementar arquitetura Bronze / Silver / Gold
- Traduzir dados em métricas de negócio
- Criar tabelas prontas para visualização e dashboards

---
## 📁 Estrutura dos Dados

├── notebooks
│   ├── setup
│   ├── bronze
│   ├── silver
│   └── gold
│
├── dashboards
│   ├── README.md
│   └── images
|       └── kpi_dashboard
│       └── kpi_dashboard_001.png
|       └── kpi_dashboard_002.png
|       └── kpi_dashboard_003.png
│
├── docs
│   ├── DATA_DICTIONARY_NYC_YELLOW_TAXI.md
│   └── GOLD_LAYER_DOCUMENTATION.md
│
└── README.md

---

## 🧱 Arquitetura de Dados

- **Bronze:** ingestão dos arquivos CSV originais
- **Silver:** limpeza, padronização e regras de qualidade
- **Gold:** KPIs e agregações para consumo analítico

---

## 📊 Principais KPIs
- Total de corridas
- Receita total
- Ticket médio
- Receita por dia e por hora
- Análise por tipo de pagamento
- Relação entre distância e valor da corrida

---

## 🛠️ Tecnologias Utilizadas
- Databricks
- Apache Spark
- SQL
- Python
- GitHub

---

## 📌 Fonte dos Dados
NYC Yellow Taxi Trip Records 2024 [https://www.kaggle.com/datasets/maxkharlam/nyc-yellow-taxi-trip-records-2024]

