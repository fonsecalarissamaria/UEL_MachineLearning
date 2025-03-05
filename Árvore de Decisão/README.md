# Análise de Dados com Árvores de Decisão

Este notebook foi desenvolvido para a disciplina de **Machine Learning** e tem como objetivo demonstrar o uso de algoritmos de aprendizado supervisionado, especificamente **Árvores de Decisão**, para análise de dois conjuntos de dados distintos.

## Estrutura do Notebook

O notebook é dividido nas seguintes seções:

1. **Carregar pacotes**: Aqui são carregados os pacotes essenciais para a execução das análises, como `pandas`, `numpy`, e os módulos da biblioteca `scikit-learn`.

2. **Carregar o conjunto de dados**: O notebook carrega três conjuntos de dados:
   - `student-mat.csv`: Dados relacionados ao desempenho dos alunos em Matemática.
   - `student-por.csv`: Dados relacionados ao desempenho dos alunos em Português.
   - `ObesityDataSet_raw_and_data_sinthetic.csv`: Dados relacionados ao índice de obesidade e características físicas de indivíduos.

3. **Árvore de Decisão**: Esta seção define e avalia um modelo de **Árvore de Decisão** utilizando os conjuntos de dados carregados. O modelo é treinado, avaliado e a acurácia do treinamento e teste são exibidas.

4. **Análise dos Conjuntos de Dados**:
   - **Conjunto 1: Dados sobre obesidade**: O modelo é aplicado ao conjunto de dados de obesidade, com codificação da variável alvo e seleção de atributos numéricos.
   - **Conjunto 2: Desempenho estudantil**: O desempenho dos alunos em Matemática é analisado utilizando faixas para a variável alvo `G1` (nota do primeiro período).

5. **Avaliação dos Modelos**: O desempenho dos modelos de Árvores de Decisão é avaliado para ambos os conjuntos de dados, apresentando métricas como acurácia, erro e relatórios de classificação.

## Pacotes Necessários

Este notebook requer os seguintes pacotes Python para funcionar corretamente:

- `pandas`: Para manipulação e análise de dados.
- `numpy`: Para operações numéricas.
- `scikit-learn`: Para aplicar o modelo de Árvore de Decisão e outras ferramentas de aprendizado de máquina.
- `IPython`: Para configurar a visualização dos dados.

Você pode instalar os pacotes necessários utilizando o seguinte comando:

```bash
pip install pandas numpy scikit-learn
```

## Como Executar

1. Abra este notebook em um ambiente Jupyter.
2. Certifique-se de ter os arquivos CSV de dados (`student-mat.csv`, `student-por.csv`, `ObesityDataSet_raw_and_data_sinthetic.csv`) no diretório correto.
3. Execute cada célula sequencialmente para carregar os pacotes, carregar os dados, treinar o modelo e avaliar o desempenho.

## Resultados Esperados

O notebook irá apresentar as seguintes informações:

- As primeiras linhas dos conjuntos de dados carregados.
- O desempenho das Árvores de Decisão para os dois conjuntos de dados, incluindo métricas como erro e acurácia para os conjuntos de treinamento e teste.
- O relatório de classificação detalhado do modelo de decisão.
