# 📊 iFood EDA Estatísticas Descritivas

## Visão Geral do Projeto

Este repositório contém um projeto de **Análise Exploratória de Dados (EDA)** focado em um conjunto de dados de restaurantes da plataforma iFood, utilizando a biblioteca **Pandas** no Python. O objetivo principal é extrair estatísticas descritivas cruciais para entender a distribuição e a tendência central de variáveis-chave, como taxas de entrega, tempo de entrega e distância.

O notebook principal (`calculos_estatisticos.ipynb`) demonstra técnicas essenciais de preparação e resumo de dados, incluindo a classificação de variáveis numéricas e categóricas, e o cálculo de medidas de tendência central (média, mediana e moda).

O trabalho consta no escopo da disciplina "Estatística com Python", da formação em ciências de dados, da DNC.

## 💾 Sobre os Dados

O conjunto de dados original possuía **406.400 registros** e um tamanho de aproximadamente **335MB**.

Para facilitar o *upload*, o gerenciamento de versões via Git e o acesso rápido ao projeto, o arquivo **`ifood-restaurants-february-2021.csv`** foi **reduzido**.

* **Nota:** Se o arquivo de dados incluído no repositório for apenas uma amostra, o **`README.md`** deve indicar que a análise completa apresentada abaixo foi realizada sobre o conjunto de dados original.

## 🛠️ Tecnologias Utilizadas

* **Python**
* **Pandas**
* **NumPy**
* **Jupyter Notebook**

## 💡 Principais Objetivos

1.  Carregar e inspecionar o dataset (utilizando `pd.info()`).
2.  Selecionar colunas relevantes para a análise (`delivery_fee`, `distance`, `delivery_time`, `category`, etc.).
3.  Classificar as variáveis em **Numéricas** e **Categóricas**.
4.  Gerar um **Resumo Estatístico Descritivo** completo para as variáveis numéricas (utilizando a função `describe()`).
5.  Calcular e interpretar a **Moda** para as variáveis categóricas.
6.  Calcular a **Média** e **Mediana** individualmente para reforçar a compreensão das distribuições.

## 🔎 Análise e Insights (Baseado na Função `describe()`)

A análise estatística descritiva, gerada principalmente pela função `df.describe()`, revelou as seguintes informações sobre os **mais de 406 mil registros**:

### Dados Numéricos

| Métrica | delivery_fee (Taxa de Entrega) | distance (Distância) | delivery_time (Tempo de Entrega) |
| :--- | :--- | :--- | :--- |
| **Média** | R$ 6.80 | 4.22 km | 47.43 minutos |
| **Mediana** (50%) | R$ 6.00 | 3.08 km | 45.00 minutos |
| **Máximo** | R$ 35.00 | 11810.19 km | 5050.00 minutos |
| **Desvio Padrão** | 4.31 | 68.33 | 19.66 |

* **Tendência Central:** A **taxa de entrega mediana (R$ 6,00)** e o **tempo de entrega mediano (45 min)** são ligeiramente inferiores às suas respectivas médias, indicando que a maioria dos pedidos se concentra em valores menores, mas existem outliers (valores extremos) que elevam a média.
* **Outliers:** Os valores máximos extremamente altos para `distance` e `delivery_time` (11810 km e 5050 min) sugerem a presença de **outliers** ou erros de entrada de dados que precisarão de tratamento em etapas futuras de limpeza.
* **Dispersão:** O desvio padrão de 19.66 para `delivery_time` mostra uma variação considerável nos tempos de entrega.

### Dados Categóricos (Moda)

| Variável | Moda (Valor Mais Frequente) | Observação |
| :--- | :--- | :--- |
| **category** | Lanches | A categoria "Lanches" é a mais popular na base. |
| **price_range** | CHEAPEST | A maioria dos restaurantes se enquadra na faixa de preço "Mais Barato" (`CHEAPEST`). |

---
