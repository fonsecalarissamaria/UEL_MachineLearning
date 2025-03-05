# UEL_MachineLearning

Este repositório contém diversos notebooks relacionados a projetos de aprendizado de máquina, cada um focado em diferentes abordagens e conjuntos de dados. Os projetos exploram desde técnicas clássicas até aprendizado profundo, utilizando modelos supervisionados para resolver problemas práticos. Abaixo estão descrições breves de cada notebook presente nesta pasta:

### 1. **Classificação de Resíduos**
Objetivo: Classificar imagens de resíduos utilizando diferentes modelos de aprendizado de máquina. Este projeto utiliza um conjunto de dados com imagens de vários tipos de resíduos e aplica três abordagens distintas para a classificação:
- Redes Neurais Convolucionais (CNN)
- K-Nearest Neighbors (KNN)
- Random Forest (RF)

---

### 2. **Classificação da Qualidade dos Vinhos**
Objetivo: Analisar e comparar o desempenho de dois modelos de classificação — Random Forest e Regressão Logística — para prever a qualidade de vinhos com base em um conjunto de dados de características físico-químicas. O desempenho dos modelos é avaliado utilizando métricas como acurácia, precisão e revocação. O melhor modelo é salvo para uso futuro.

---

### 3. **MNIST Classificação**
Objetivo: Implementar um modelo de aprendizado profundo para a classificação de imagens do conjunto de dados MNIST utilizando TensorFlow e Keras. O modelo é uma rede neural feedforward simples, treinada para reconhecer dígitos manuscritos em imagens de 28x28 pixels. O desempenho do modelo é avaliado com base em métricas como acurácia, perda e matriz de confusão. Além disso, gráficos de acurácia e perda durante o treinamento são gerados para análise.

---

### 4. **Árvore de Decisão**
Objetivo: Demonstrar o uso do algoritmo de Árvores de Decisão para análise de dois conjuntos de dados distintos. Este notebook explora a aplicação de Árvores de Decisão em problemas de classificação supervisionada e compara os resultados de modelos treinados com diferentes parâmetros.

---

### Pré-requisitos

Para executar os notebooks, é necessário ter o seguinte ambiente instalado:

- Python 3.x
- Bibliotecas Python:
  - `numpy`
  - `pandas`
  - `scikit-learn`
  - `matplotlib`
  - `seaborn`
  - `tensorflow` (para o notebook MNIST)
  - `joblib` (para salvar o modelo treinado)
