# Camada Gold — Documentação Analítica

A camada Gold contém tabelas analíticas prontas para consumo por dashboards, relatórios e análises de negócio.
Essas tabelas foram construídas a partir da camada Silver, após processos de limpeza e validação de qualidade.

## Objetivo da Camada Gold
- Disponibilizar KPIs consolidados
- Facilitar análises recorrentes
- Reduzir complexidade para consumo analítico
- Servir como base para visualizações e dashboards

---

## Tabelas Disponíveis

### 1. taxi_trip_gold.kpi_overall
**Descrição:** KPIs gerais do serviço de táxi.

**Granularidade:** Visão global (sem dimensão temporal)

**Principais métricas:**
- total_trips
- total_revenue
- avg_ticket
- avg_distance
- avg_tip

**Uso recomendado:**
- Cards de indicadores
- Visão executiva

---

### 2. taxi_trip_gold.kpi_daily_revenue
**Descrição:** Receita e volume de corridas por dia.

**Granularidade:** Dia

**Principais métricas:**
- total_trips
- total_revenue
- avg_ticket

**Uso recomendado:**
- Análise temporal
- Tendência de receita

---

### 3. taxi_trip_gold.kpi_hourly_revenue
**Descrição:** Receita e volume por hora do dia.

**Granularidade:** Hora

**Uso recomendado:**
- Identificação de horários de pico
- Planejamento operacional

---

### 4. taxi_trip_gold.kpi_payment_behavior
**Descrição:** Análise de comportamento por tipo de pagamento.

**Dimensão principal:** payment_type

**Uso recomendado:**
- Estratégias de pagamento
- Análise de gorjetas

---

### 5. taxi_trip_gold.kpi_distance_analysis
**Descrição:** Relação entre distância da corrida e valor pago.

**Dimensão principal:** Faixa de distância

**Uso recomendado:**
- Avaliação de precificação
- Análise de ticket médio
