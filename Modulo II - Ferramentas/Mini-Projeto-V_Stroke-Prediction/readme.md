# Classificador de AVC

Este é um mini projeto focado em criar um classificador para prever se um paciente é suscetível a ter um AVC (Acidente Vascular Cerebral) com base em dados disponíveis. Os dados para este projeto estão disponíveis no Kaggle em [Stroke Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset).

## Objetivo
O objetivo principal deste projeto é desenvolver um modelo capaz de analisar os dados de vários pacientes e determinar se um paciente é suscetível a ter um AVC ou não.

## Bibliotecas e Algoritmos Utilizados

### Bibliotecas

- **Pandas:** Para manipulação e análise de dados.
- **NumPy:** Para computação numérica e operações em arrays.
- **Matplotlib e Seaborn:** Para visualização de dados.
- **Missingno:** Para visualização de dados ausentes.

### Ferramentas de Aprendizado de Máquina (Scikit-learn)

- **Algoritmos de Classificação:**
  - RandomForest, AdaBoost, GradientBoosting, LogisticRegression, KNeighbors, DecisionTree, SVC, XGBoost, LGBM.
- **Pré-processamento de Dados:**
  - LabelEncoder, MinMaxScaler.
- **Avaliação de Modelos:**
  - accuracy_score, precision_score, recall_score, f1_score, roc_auc_score, confusion_matrix, classification_report, roc_curve.
- **Validação Cruzada:**
  - GridSearchCV, cross_val_score.

### Ferramenta para Tratar Dados Desbalanceados

- **SMOTE (do Imbalanced-learn):** Para oversampling sintético em conjuntos de dados desbalanceados. O uso do SMOTE é especialmente relevante devido à disparidade entre os casos de AVC e não AVC na base de dados, garantindo uma representação mais equilibrada durante o treinamento do modelo.

## Passos

1. **Preparar dados para uso:**
   - Ler os dados do conjunto de dados disponível.
   - Limpar os dados, tratando valores ausentes e outliers, se necessário.
   - Normalizar os dados, se aplicável, para garantir que todas as características tenham a mesma escala.
   - Separar os dados em conjuntos de treinamento e teste.

2. **Plotar informações para ganhar insights:**
   - Visualizar dados relevantes, como distribuição de idade, gênero, pressão arterial, etc., para obter insights sobre padrões e correlações.
   ![Pie Chart - Relação AVCs e Doença Cardíaca](/img/AVC_vs_Doenca_cardiaca.png)
   ![Matriz de Correlação entre Atributos](/img/correlacao_atributos.png)

3. **Utilizar um classificador:**
   - Selecionar um algoritmo de classificação adequado, como Árvores de Decisão, Random Forest, SVM, etc., para construir o modelo de previsão.
   - Treinar o modelo com o conjunto de treinamento preparado.

4. **Criar um pipeline (opcional):**
   - Se necessário, criar um pipeline de pré-processamento de dados e modelagem para automatizar o fluxo de trabalho e torná-lo mais eficiente.

5. **Utilizar validação cruzada:**
   - Utilizar técnicas de validação cruzada, como cross-validation, para avaliar o desempenho do modelo e garantir sua generalização para dados não vistos.
   <div style="display: flex;">
    <img src="/img/AUC-Random_Forest.png" alt="AUC Curve" style="width: 45%; height: 50%; object-fit: contain;">
    <img src="/img/matriz_confusao-Random_Forest.png" alt="Matriz de Confusão" style="width: 45%; height: 45%; object-fit: contain;">
   </div>

## Como usar
- Os dados do Kaggle já estão disponíveis na pasta "data".
- Lembre-se de instalar os pacotes que o notebook utiliza previamente.
- Execute o código fornecido no notebook para seguir os passos mencionados acima.
- Analise os resultados do modelo e faça ajustes, se necessário, para melhorar a precisão da previsão.
