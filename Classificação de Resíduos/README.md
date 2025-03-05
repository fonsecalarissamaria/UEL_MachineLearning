# 🚮 Classificação de Resíduos com Modelos de Machine Learning

Este projeto tem como objetivo classificar imagens de resíduos utilizando diferentes modelos de aprendizado de máquina. Utilizamos um conjunto de dados com imagens de diferentes tipos de resíduos e aplicamos três abordagens distintas para a classificação: Redes Neurais Convolucionais (CNN), K-Nearest Neighbors (KNN) e Random Forest (RF).

## Estrutura do Projeto

O código está dividido nas seguintes etapas:

1. **Carregamento das Imagens**: As imagens de resíduos são carregadas a partir de diretórios que representam diferentes classes de resíduos.
2. **Pré-processamento**: As imagens são redimensionadas para o tamanho de 128x128 pixels e normalizadas para o intervalo [0, 1].
3. **Codificação dos Rótulos**: As classes de resíduos são codificadas para valores numéricos utilizando o `LabelEncoder` e convertidas para formato one-hot encoding, adequado para a rede neural.
4. **Divisão dos Dados**: Os dados são divididos em conjuntos de treinamento, validação e teste.
5. **Criação de Modelos**: Três modelos diferentes são treinados e avaliados:
   - **CNN (Rede Neural Convolucional)**: Usada para processamento direto de imagens.
   - **KNN (K-Nearest Neighbors)**: Um modelo de classificação baseado em proximidade.
   - **Random Forest**: Um modelo de árvore de decisão em conjunto com outros classificadores.
6. **Avaliação e Comparação**: O desempenho de cada modelo é avaliado com base na acurácia e no F1-score. Em seguida, uma comparação entre os modelos é feita usando gráficos.

## Requisitos

Para executar este código, você precisará dos seguintes pacotes Python:

- `numpy`
- `pandas`
- `tensorflow`
- `scikit-learn`
- `matplotlib`
- `seaborn`

Você pode instalar as dependências utilizando o `pip`:

```bash
pip install numpy pandas tensorflow scikit-learn matplotlib seaborn
```

## Etapas de Execução

1. **Carregar e Processar as Imagens**: O código carrega imagens a partir dos diretórios definidos no `data_path`. As imagens são normalizadas para o intervalo [0, 1] e transformadas em arrays numpy.
2. **Treinamento do Modelo CNN**: Um modelo CNN simples é treinado com as imagens de treinamento e avaliado no conjunto de teste.
3. **Treinamento do Modelo KNN**: As imagens são achatadas em vetores 1D e um modelo KNN é treinado para classificação.
4. **Treinamento do Modelo Random Forest**: O modelo Random Forest é treinado com os mesmos dados usados para o KNN.
5. **Avaliação dos Modelos**: O desempenho de todos os modelos é avaliado e comparado utilizando métricas como acurácia e F1-score.
6. **Visualização**: Resultados de desempenho dos modelos são visualizados com gráficos de barras e matrizes de confusão.

## Resultados

- **CNN**: A acurácia no conjunto de teste é calculada e o modelo é salvo em um arquivo `.keras`.
- **KNN e Random Forest**: As acurácias desses modelos são avaliadas e os resultados são apresentados, incluindo a classificação detalhada de cada classe.

## Como Usar

1. Clone este repositório ou faça o download do código.
2. Coloque suas imagens de resíduos em pastas dentro do diretório `data_path`, onde cada subpasta corresponde a uma classe de resíduo.
3. Execute o código Python. Os resultados de avaliação serão exibidos no terminal e gráficos serão gerados para comparar o desempenho dos modelos.

## Salvamento do Modelo

O modelo CNN treinado é salvo no formato `.keras`:

```python
cnn_model.save('cnn_realwaste_model.keras')
```
