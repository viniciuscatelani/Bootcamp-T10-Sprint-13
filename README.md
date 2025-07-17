# Bootcamp-T10-Sprint-13

# 🧠 Previsão de Demanda de Táxis por Hora

Este projeto tem como objetivo construir um modelo de machine learning capaz de prever a quantidade de pedidos de táxi para a próxima hora, com base em dados históricos da empresa **Sweet Lift Taxi**.

O desafio consiste em reduzir o erro de previsão (RMSE) para um valor inferior a 48.

## 📂 Sobre os Dados

- **Fonte**: Arquivo `data/taxi.csv`
- **Colunas**:
  - `num_orders`: número de pedidos de táxi.
- **Índice**: timestamps de data e hora.

Os dados originais foram reamostrados para intervalos de **1 hora** utilizando `resample('1H')`.

## 🧪 Etapas do Projeto

1. **Importação e preparação dos dados**
2. **Reamostragem horária**
3. **Análise exploratória e decomposição temporal**
4. **Criação de variáveis e features de série temporal**
5. **Divisão entre treino, validação e teste**
6. **Treinamento de modelos (XGBoost e LightGBM)**
7. **Busca de hiperparâmetros (RandomizedSearchCV)**
8. **Avaliação final com RMSE**

## 🔧 Tecnologias Utilizadas

- Python
- Pandas / NumPy
- scikit-learn
- XGBoost / LightGBM
- Statsmodels
- Matplotlib

## 📈 Modelos Treinados

Foram utilizados dois modelos principais:

- `XGBRegressor`
- `LGBMRegressor`

Ambos foram avaliados com validação temporal (`TimeSeriesSplit`) e calibrados com `RandomizedSearchCV`.

## 🎯 Métrica Avaliada

- **RMSE (Root Mean Squared Error)**: métrica principal para avaliar a performance dos modelos.
- **Objetivo**: RMSE no conjunto de teste **inferior a 48**.

## ✅ Resultados

- O modelo treinado foi capaz de atingir um desempenho **satisfatório**, com RMSE abaixo do limite estipulado.
- Técnicas como decomposição de séries temporais e criação de variáveis de defasagem foram importantes para melhorar a performance preditiva.

## 🚀 Como Executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/seuusuario/seuprojeto.git
   cd seuprojeto
   ```
2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```
3. Execute o notebook:
   ```bash
   jupyter notebook sprint\ 13.ipynb
   ```
