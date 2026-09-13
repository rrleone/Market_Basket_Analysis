# Market Basket Analysis

## 📊 Sobre o projeto

Projeto de **Market Basket Analysis (MBA)** desenvolvido em Python com o objetivo de identificar associações entre produtos comprados na mesma transação.

A análise busca transformar o comportamento de compra em informações que podem apoiar estratégias de **cross-selling, recomendação de produtos e composição de ofertas**.

## 🎯 Objetivo

Investigar padrões de compra e identificar regras de associação entre produtos utilizando o algoritmo **Apriori** e as métricas:

- **Support**
- **Confidence**
- **Lift**

## 🗂️ Dataset

O projeto utiliza o conjunto de dados **Instacart Market Basket Analysis**, composto pelas tabelas:

| Arquivo | Descrição |
|---|---|
| `aisles.csv` | Corredores/categorias de produtos |
| `departments.csv` | Departamentos |
| `orders.csv` | Informações dos pedidos |
| `products.csv` | Cadastro de produtos |
| `order_products__prior.csv` | Produtos dos pedidos anteriores |
| `order_products__train.csv` | Produtos do conjunto de treino |

A base `order_products__prior.csv` é a principal fonte transacional utilizada na construção das cestas.

> **Dados brutos:** os arquivos originais não são armazenados neste repositório devido ao tamanho do dataset. Para reproduzir integralmente a análise, é necessário obter os dados originais e colocá-los na pasta `dados/`.

## 🔎 Metodologia

O projeto segue as seguintes etapas:

1. Carregamento dos dados;
2. Inspeção das tabelas;
3. Análise exploratória;
4. Verificação de valores ausentes;
5. Integração das tabelas;
6. Análise de pedidos, produtos, departamentos e comportamento de recompra;
7. Construção das cestas de produtos;
8. Aplicação do algoritmo Apriori;
9. Avaliação das regras de associação;
10. Interpretação dos resultados sob a perspectiva de negócio.

### Formação das transações

A tabela `order_products__prior.csv` possui uma linha por item associado a um pedido. Os produtos são agrupados por `order_id`, formando uma cesta de produtos para cada pedido.

O projeto registrou **3.214.874 transações** após essa preparação.

### Aplicação do Apriori

Para controlar o processamento, o Apriori foi aplicado sobre uma **amostra de 500.000 transações**.

Foram avaliadas duas configurações principais:

- Support mínimo = **0,01** e Confidence mínimo = **0,20**
- Support mínimo = **0,005** e Confidence mínimo = **0,20**

## 📐 Métricas

### Support

Indica a proporção de transações que contém simultaneamente os itens da associação.

### Confidence

Para uma regra `A → B`, representa a proporção de transações que contêm `B` entre aquelas que contêm `A`.

### Lift

Compara a ocorrência conjunta dos produtos com a ocorrência esperada considerando a frequência individual dos itens.

- **Lift > 1:** associação positiva;
- **Lift = 1:** ausência de associação adicional;
- **Lift < 1:** associação negativa.

## 📈 Principais resultados

Entre as regras apresentadas na análise, destacam-se:

| Produto A | Produto B | Confidence | Lift |
|---|---|---:|---:|
| Organic Cilantro | Limes | 25,04% | **5,74** |
| Organic Garlic | Organic Yellow Onion | 20,11% | **5,69** |
| Organic Lemon | Organic Hass Avocado | 23,99% | **3,62** |
| Organic Cucumber | Organic Hass Avocado | 21,54% | **3,25** |
| Organic Raspberries | Organic Strawberries | 24,86% | **3,01** |

Essas associações apresentam Lift superior a 1, indicando associação positiva entre os produtos dentro da amostra analisada.

## 💡 Insights de negócio

Os resultados sugerem oportunidades para:

- recomendações de produtos relacionados;
- estratégias de cross-selling;
- criação de combinações de produtos;
- organização de ofertas;
- apoio à personalização da experiência de compra.

As regras de associação, entretanto, não devem ser interpretadas isoladamente. Uma aplicação comercial exigiria também considerar fatores como **margem, estoque, preço, disponibilidade e contexto da operação**.

## 🛠️ Tecnologias utilizadas

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Efficient Apriori
- Watermark

## 📁 Estrutura sugerida

```text
Market-Basket-Analysis/
│
├── README.md
├── notebooks/
│   └── MBA.ipynb
│
├── reports/
│   └── MBA.pdf
│
├── dados/
│   └── README.md
│
└── requirements.txt
```

## ▶️ Como executar

1. Obter os dados originais do dataset.
2. Colocar os seis arquivos CSV na pasta `dados/`.
3. Criar um ambiente Python.
4. Instalar as dependências listadas em `requirements.txt`.
5. Abrir `notebooks/MBA.ipynb`.
6. Executar as células na ordem apresentada.

> A execução integral depende da disponibilidade do `order_products__prior.csv` e dos demais arquivos de dados.

## ⚠️ Reprodutibilidade e validação

Os resultados apresentados neste projeto foram **auditados quanto à consistência metodológica e matemática com base no notebook e nos outputs registrados**.

As métricas de associação foram verificadas a partir das fórmulas utilizadas no próprio projeto.

A execução integral do notebook não foi refeita nesta etapa porque o arquivo original `order_products__prior.csv` não está atualmente disponível no ambiente de trabalho.

Portanto, o projeto não afirma que os resultados foram reexecutados independentemente nesta revisão.

## 📄 Materiais

- **Notebook:** análise completa em Jupyter Notebook.
- **PDF:** versão documentada da análise e dos resultados.

## 👤 Autor

**Renato Leone**

Projeto desenvolvido para demonstrar a aplicação prática de técnicas de **Análise de Dados e Market Basket Analysis com Python**.
