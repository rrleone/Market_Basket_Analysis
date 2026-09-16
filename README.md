# 📊 Customer Churn Analytics

## 🎯 Problema de negócio

A empresa deseja entender o comportamento de churn dos clientes e identificar quais perfis apresentam maiores taxas de cancelamento.

A análise busca transformar os dados de clientes em informações que apoiem decisões de retenção, priorização de segmentos de risco e acompanhamento dos principais indicadores de churn.

---

## 🗂️ Sobre os dados

- **Fonte:** Dataset público de Customer Churn disponibilizado via Kaggle
- **Tamanho:** 7.043 clientes e 19 variáveis
- **Tipo de análise:** Customer Churn / Customer Retention
- **Unidade de análise:** cliente

### Principais informações analisadas

- Identificação do cliente
- Perfil demográfico
- Partner e Dependents
- Tenure
- Tipo de contrato
- Serviços de internet
- Serviços adicionais
- Monthly Charges
- Total Charges
- Forma de pagamento
- Status de Churn

---

## 🛠️ Ferramentas utilizadas

- **Linguagem:** Python
- **Análise:** Pandas / NumPy
- **Ambiente:** Jupyter Notebook / VS Code
- **Visualização exploratória:** Matplotlib / Seaborn
- **BI:** Power BI
- **Transformação:** Power Query
- **Modelagem e métricas:** DAX
- **Versionamento:** Git / GitHub

---

## 🔍 Etapas da análise

1. **Data Profiling** — entendimento da estrutura, tipos de dados, dimensões e características das variáveis.
2. **Data Quality** — verificação de valores ausentes, inconsistências, duplicidades e qualidade das variáveis.
3. **Análise exploratória (EDA)** — investigação do comportamento de churn segundo perfil, tenure, contrato, serviços e forma de pagamento.
4. **Feature Engineering** — criação de agrupamentos e variáveis analíticas, incluindo faixas de tenure e perfil de risco.
5. **Análise de Churn** — cálculo de clientes churn, taxa de churn e análise dos principais segmentos.
6. **Customer Segmentation** — análise dos clientes segundo tempo de relacionamento, mensalidade e características contratuais.
7. **Business Insights** — transformação dos resultados da análise em informações relevantes para retenção.
8. **Power BI Dashboard** — construção de um dashboard executivo com três páginas de análise.

---

## 📈 Principais insights

- **26,54%** dos clientes da base apresentam churn.
- Clientes com contrato **Month-to-month** apresentam taxa de churn de **42,7%**.
- A faixa de relacionamento de **0–12 meses** apresenta taxa de churn de **47,4%**.
- Clientes com serviço de internet **Fiber optic** apresentam taxa de churn de **41,9%**.
- **Electronic check** apresenta a maior taxa de churn entre as formas de pagamento analisadas, com **45,29%**.
- Clientes classificados como **Senior Citizen** apresentam taxa de churn de **41,7%**, contra **23,6%** entre os demais clientes.
- Clientes **sem dependents** apresentam taxa de churn de **31,28%**, enquanto clientes com dependents apresentam **15,45%**.

Os resultados representam associações observadas na base analisada e não implicam, isoladamente, relação de causalidade.

---

## 🖼️ Prévia do dashboard

O projeto possui três páginas no Power BI:

### 01 — Executive Overview

Visão executiva dos principais KPIs e dos principais indicadores associados ao churn.

### 02 — Customer Profile & Churn Drivers

Análise do perfil dos clientes e dos principais fatores associados ao churn.

### 03 — Churn Risk & Customer Segmentation

Análise de risco, segmentação de clientes e visualização do perfil individual dos clientes.

> As imagens finais do dashboard serão disponibilizadas na pasta `images/`.

---

## ✅ Conclusão e recomendação

A análise indica concentração de churn em determinados segmentos, especialmente entre clientes com contratos Month-to-month, menor tempo de relacionamento e determinados serviços e formas de pagamento.

Como oportunidade de negócio, recomenda-se utilizar esses segmentos como base para estratégias de retenção e acompanhamento direcionado, validando posteriormente quais ações apresentam melhor resultado sobre a permanência dos clientes.

---

## 📁 Estrutura do repositório

```text
Customer-Churn-Analytics/
│
├── data/
│   └── README.md
│
├── notebooks/
│   ├── 01_data_profiling.ipynb
│   ├── 02_data_quality.ipynb
│   ├── 03_eda_churn.ipynb
│   └── 04_feature_engineering.ipynb
│
├── images/
│   ├── dashboard_page_01.png
│   ├── dashboard_page_02.png
│   └── dashboard_page_03.png
│
├── powerbi/
│   └── Customer_Churn_Analytics.pbix
│
├── requirements.txt
└── README.md
```

---

## 🚀 Como reproduzir

Clone o repositório:

```bash
git clone https://github.com/rrleone/Customer-Churn-Analytics.git
cd Customer-Churn-Analytics
```

Instale as dependências:

```bash
pip install -r requirements.txt
```

Abra os notebooks na ordem indicada em `notebooks/` e execute as etapas da análise.

O dashboard pode ser aberto no Power BI Desktop a partir do arquivo disponível em `powerbi/`.

---

## 👤 Autor

**Renato Leone**

Analista de Dados | BI | SQL | Power BI | Python | PostgreSQL

GitHub: https://github.com/rrleone

