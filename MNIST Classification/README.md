# 9️⃣ Classificação do conjunto de dados MNIST

## Visão Geral

Este notebook implementa um modelo de aprendizado profundo para a classificação de imagens do conjunto de dados MNIST utilizando o TensorFlow e Keras. O modelo é uma rede neural feedforward simples que é treinada para reconhecer dígitos manuscritos em imagens de 28x28 pixels. Após o treinamento, o desempenho do modelo é avaliado no conjunto de teste, e as métricas de desempenho, como acurácia, perda e uma matriz de confusão, são exibidas. Além disso, gráficos de acurácia e perda durante o treinamento são gerados para análise.

## Requisitos

Certifique-se de ter as bibliotecas abaixo instaladas antes de executar este notebook:

- `tensorflow`
- `numpy`
- `matplotlib`
- `sklearn`
- `idx2numpy`

Você pode instalar essas dependências usando o comando pip:

```bash
pip install tensorflow numpy matplotlib scikit-learn idx2numpy
```

## Funcionalidade

1. **Carregamento de Dados**
   - O notebook carrega o conjunto de dados MNIST a partir de arquivos `.idx3-ubyte` (imagens) e `.idx1-ubyte` (rótulos).
   - Verifica se os arquivos estão presentes no diretório atual antes de prosseguir.

2. **Pré-processamento de Dados**
   - As imagens são normalizadas, convertendo os valores de pixel de 0-255 para o intervalo de 0-1.
   
3. **Visualização Inicial**
   - Exibe uma amostra de uma imagem do conjunto de treinamento com seu rótulo.

4. **Construção do Modelo**
   - O modelo é uma rede neural simples com:
     - Uma camada de entrada que achata as imagens de 28x28 para um vetor de 784 elementos.
     - Duas camadas ocultas com 128 e 64 neurônios, respectivamente, e a função de ativação ReLU.
     - Uma camada de saída com 10 neurônios, usando a função de ativação Softmax para a classificação.

5. **Treinamento do Modelo**
   - O modelo é treinado por 10 épocas utilizando a função de perda `sparse_categorical_crossentropy` e o otimizador `adam`.

6. **Avaliação do Modelo**
   - O desempenho do modelo é avaliado no conjunto de teste, e a perda e acurácia são exibidas.
   - O modelo gera previsões para as imagens de teste e as compara com os rótulos reais utilizando a função `classification_report` do Scikit-learn.
   
7. **Matriz de Confusão**
   - Uma matriz de confusão é exibida para visualizar os erros de classificação entre os diferentes dígitos.

8. **Visualização do Treinamento**
   - Gráficos de acurácia e perda durante o treinamento são gerados para análise visual do desempenho do modelo ao longo das épocas.

## Como Usar

1. Coloque os arquivos de dados MNIST (`train-images.idx3-ubyte`, `train-labels.idx1-ubyte`, `t10k-images.idx3-ubyte`, `t10k-labels.idx1-ubyte`) no mesmo diretório do notebook.
2. Execute o notebook.
3. O modelo será treinado e a avaliação será exibida.

## Exemplo de Saída

Ao final da execução, o notebook exibirá a acurácia do modelo no conjunto de teste, a matriz de confusão, e gráficos com a evolução da acurácia e perda ao longo das épocas. Além disso, as métricas de desempenho, como precisão, recall e F1-score, serão exibidas no relatório de classificação.
