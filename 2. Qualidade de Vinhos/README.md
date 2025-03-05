# 🍷 Análise e Comparação de Modelos de Classificação para Previsão de Qualidade de Vinhos

Este notebook realiza a análise e comparação de dois modelos de classificação — **Random Forest** e **Regressão Logística** — para prever a qualidade de vinhos com base em um conjunto de dados de características físico-químicas dos vinhos. O objetivo é avaliar o desempenho dos modelos utilizando métricas como acurácia, precisão e revocação, além de salvar o melhor modelo para uso futuro.

## Conjunto de Dados

Os dados utilizados neste notebook são provenientes de dois arquivos CSV:

- **winequality-red.csv**: Contém informações sobre vinhos tintos.
- **winequality-white.csv**: Contém informações sobre vinhos brancos.

Cada conjunto contém as seguintes variáveis:
- **features**: Características físico-químicas do vinho (como pH, acidez, etc.)
- **quality**: A nota de qualidade do vinho, variável alvo.
- **type**: O tipo de vinho (0 para tinto, 1 para branco).

## Etapas do Processo

1. **Carregamento dos Dados**: Os conjuntos de dados para vinhos tinto e branco são carregados e combinados.
2. **Pré-processamento**:
   - Verificação de valores ausentes.
   - Normalização dos dados utilizando o **StandardScaler**.
   - Separação dos dados em conjunto de treinamento e teste.
3. **Treinamento e Avaliação**:
   - Os modelos **Random Forest** e **Regressão Logística** são treinados com validação cruzada utilizando a técnica de subamostragem aleatória.
   - Para cada modelo, são calculadas as métricas: **acurácia**, **precisão** e **revocação**.
4. **Comparação de Desempenho**: As métricas médias de cada modelo são comparadas em um gráfico.
5. **Salvamento do Melhor Modelo**: O modelo com o melhor desempenho (Random Forest) é salvo em um arquivo `.pkl` para uso futuro.

## Pacotes Utilizados

- `numpy`: Para manipulação de arrays e cálculos numéricos.
- `pandas`: Para manipulação e análise de dados.
- `sklearn`: Para treinamento, avaliação e validação de modelos de machine learning.
- `matplotlib`: Para visualização de gráficos.
- `joblib`: Para salvar o modelo treinado.

## Resultados

Após a execução do notebook, você verá as médias das métricas (acurácia, precisão e revocação) para ambos os modelos. Além disso, um gráfico será gerado para comparar o desempenho de **Random Forest** e **Regressão Logística**.

## Como Usar

1. Clone este repositório ou baixe os arquivos necessários.
2. Execute o notebook em seu ambiente Python com as bibliotecas necessárias instaladas.
3. O modelo treinado será salvo como `best_model.pkl` na mesma pasta.

## Observações

- Certifique-se de ter os arquivos `winequality-red.csv` e `winequality-white.csv` na pasta correta.
- Caso queira utilizar o modelo salvo em uma aplicação futura, basta carregar o arquivo `best_model.pkl` com o `joblib.load()`.
