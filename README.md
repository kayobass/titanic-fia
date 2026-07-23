# Projeto Final — Aprendizado de Máquina

## Previsão de Sobrevivência dos Passageiros do Titanic

### Integrantes

- Matheuz Rozendo
- Kayo Araujo

## Fonte dos dados

Titanic Dataset, disponibilizado no Kaggle por Yasser H.

Link: https://www.kaggle.com/datasets/yasserh/titanic-dataset

## Objetivo

Desenvolver e comparar modelos de aprendizado de máquina capazes de prever se um passageiro do Titanic sobreviveu, utilizando suas características registradas no conjunto de dados.

## Tipo de tarefa

**Classificação binária** — o atributo-alvo `Survived` possui duas categorias possíveis: sobreviveu (1) ou não sobreviveu (0).

## Atributo-alvo

`Survived` — 0 = passageiro não sobreviveu, 1 = passageiro sobreviveu.

## Atributos preditivos

`Pclass`, `Sex`, `Age`, `SibSp`, `Parch`, `Fare`, `Embarked`.

## Modelos utilizados

- Baseline
- SGDClassifier
- RandomForestClassifier

## Principais resultados

| Modelo                     | Acurácia | Precisão | Revocação | F1-score |
| -------------------------- | -------- | -------- | --------- | -------- |
| Baseline (DummyClassifier) | 61,66%   | 0,00%    | 0,00%     | 0,00%    |
| SGDClassifier              | 77,81%   | 74,73%   | 64,82%    | 68,37%   |
| RandomForestClassifier     | 78,95%   | 72,95%   | 71,46%    | 72,19%   |

O RandomForestClassifier foi escolhido como modelo final por apresentar o melhor equilíbrio entre as métricas. Na avaliação final com o conjunto de teste, ele alcançou:

- **Acurácia:** 81,56%
- **Precisão:** 80,00%
- **Revocação:** 69,57%
- **F1-score:** 74,42%

## Divisão das contribuições

### Matheuz Rozendo — Análise e pré-processamento dos dados

- Identificação e descrição do problema do projeto (prever a sobrevivência no Titanic).
- Explicação do dataset e das variáveis principais.
- Análise exploratória dos dados (EDA): distribuição do atributo-alvo, sobrevivência por sexo, classe e porto de embarque, histogramas de idade e tarifa, boxplots, gráficos de dispersão e matriz de correlação.
- Pré-processamento dos dados: tratamento de valores ausentes (mediana para numéricas, moda para categóricas), transformação de variáveis categóricas com OneHotEncoder, padronização com StandardScaler, seleção de atributos e preparação dos dados para treinamento.
- Separação dos dados em treino e teste com estratificação.

### Kayo Araujo — Modelagem e avaliação

- Explicação dos modelos de aprendizado de máquina utilizados (Baseline, SGDClassifier e RandomForestClassifier).
- Treinamento dos modelos com validação cruzada.
- Comparação dos resultados obtidos entre os modelos.
- Explicação e interpretação das métricas de avaliação (acurácia, precisão, revocação, F1-score e matriz de confusão).
- Escolha do modelo final e avaliação no conjunto de teste.
- Conclusão do projeto e apresentação de possíveis melhorias.

## Como executar

1. Abra o notebook `Projeto_Titanic.ipynb` no Google Colab

- Link: https://colab.research.google.com/drive/1u9vl3JIQEBJSHlo_-mtLHG4w6PMORGY_?usp=sharing

2. Execute todas as células em ordem
3. Os dados serão carregados automaticamente via URL

## Vídeo

Link do vídeo de apresentação: https://youtu.be/NLDx0rAbSfk

## Declaração de Uso de Ferramentas de Inteligência Artificial

### Ferramenta utilizada: _ChatGPT_ e _Gemini_.

- Finalidade: Aceleração da curva de aprendizado, tradução de conceitos teóricos de ML para a prática em Python, estruturação de pipelines de pré-processamento e auxílio na interpretação de métricas de avaliação.

### Parte do trabalho em que foi utilizada:

- Análise Exploratória (EDA): A IA foi consultada para sugerir quais tipos de gráficos (ex: boxplots para idade, barras para sobrevivência por sexo) melhor representariam as distribuições e correlações dos dados do Titanic.

- Pré-processamento: Auxílio na construção do ColumnTransformer e Pipeline. A IA explicou a necessidade lógica de usar o SimpleImputer para dados faltantes (como a idade) e o OneHotEncoder para variáveis categóricas (como sexo e porto de embarque), adaptando a explicação para o nosso nível de compreensão.

- Modelagem e Avaliação: A IA atuou como um copiloto para explicar as diferenças entre os algoritmos (Baseline, SGD e Random Forest) e nos ajudou a interpretar o que significavam, na prática, métricas como Precisão, Revocação e F1-Score, guiando nossa decisão de escolher a Random Forest.

### Forma de verificação do conteúdo ou código produzido:

1. Validação Lógica e Histórica: Todo o resultado gerado pela IA foi confrontado com a lógica e com o conhecimento histórico sobre o Titanic. Por exemplo, quando a IA gerou os códigos de EDA e os gráficos mostraram que mulheres e passageiros de 1ª classe tiveram maior taxa de sobrevivência, nós validamos que isso fazia sentido histórico ("mulheres e crianças primeiro", proximidade dos botes), o que nos deu confiança na veracidade do código.

2. Execução e Teste de Erros (Debugging): O código sugerido pela IA era inserido no Jupyter Notebook e executado. Analisávamos os shapes das bases, os outputs das matrizes de confusão e os erros de sintaxe, retornando à IA para perguntar o porquê de determinado erro, aprendendo a corrigi-lo.
