# Estudo de Caso: Previsão de Câncer de Pulmão

O câncer de pulmão é uma das principais causas de morte em todo o mundo. A detecção precoce e o diagnóstico são cruciais para melhorar os resultados dos pacientes. Este estudo de caso explora o potencial de um conjunto de dados limitado contendo informações de saúde encontrados no [Kaggle](https://www.kaggle.com/datasets/shreyasparaj1/lung-cancer-dataset) para identificar fatores de risco associados ao câncer de pulmão.
# Exploração de Dados e Pré-processamento:

![newplot](https://github.com/hugomilesi/lung_cancer_gridsearch_kfold/assets/71730507/cc920ef8-9c65-4735-a8fa-a1f29d231ea9)

- Verificação da presença de dados faltantes (nulos).
- Estatísticas descritivas das variáveis numéricas.
- Conversão de letras maiúsculas para minúsculas nos nomes das colunas.
- Codificação das variáveis categóricas ('gênero' e 'câncer de pulmão') em valores numéricos.
- Visualização da distribuição de gênero e correlações entre as variáveis.
- Visualização da distribuição de cada característica por meio de histogramas.
- Verificação do desbalanceamento da variável alvo ('câncer de pulmão') e aplicação da técnica **SMOTE** para balanceamento.

# Modelagem e Avaliação:

![image](https://github.com/hugomilesi/lung_cancer_gridsearch_kfold/assets/71730507/87c8fb52-613f-4427-a147-d1d048458e95)

- Divisão dos dados em conjuntos de treinamento e teste.
- Aplicação de modelos de classificação como RandomForest, KNN, Naive Bayes, Regressão Logística e XGBoost.
- Utilização do GridSearchCV para encontrar os melhores hiperparâmetros para cada modelo.
- Treinamento dos modelos com os dados de treinamento e avaliação do desempenho utilizando métricas como acurácia, AUC e matriz de confusão.
- Visualização da importância das características para os modelos de árvore (RandomForest e XGBoost).
- Construção de curvas ROC para comparar o desempenho dos modelos.


# Validação Cruzada (K-Fold):

![image](https://github.com/hugomilesi/lung_cancer_gridsearch_kfold/assets/71730507/09ecb665-a70d-4d7f-9ee0-001eb9ff3e80)

- Avaliação do desempenho dos modelos utilizando validação cruzada com 5 folds.
- Comparação das médias das acurácias obtidas pelos modelos.


# Resultados e Conclusões:

Com base na avaliação dos modelos, observamos que o RandomForest obteve a maior acurácia média (93.51%) na validação cruzada, seguido pelo XGBoost (92.55%), Regressão Logística (91.60%), KNN (89.74%) e Naive Bayes (89.70%).
Esses resultados sugerem que modelos de floresta aleatória e gradient boosting tendem a ter melhor desempenho na previsão de câncer de pulmão com base nas características fornecidas.
Considerações Finais:

Este estudo de caso demonstra a aplicação de técnicas de pré-processamento de dados, modelagem de machine learning e avaliação de desempenho para prever o câncer de pulmão com base em características dos pacientes.
Os modelos desenvolvidos podem ser utilizados como ferramentas de apoio à decisão médica, auxiliando na identificação precoce de pacientes em risco e direcionando recursos para intervenções preventivas.
Futuros trabalhos podem explorar outras técnicas de modelagem, como redes neurais profundas, e incorporar informações adicionais, como dados genéticos e histórico familiar, para melhorar ainda mais a precisão das previsões.
