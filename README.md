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

## Como executar

1. Abra o notebook `Projeto_Titanic.ipynb` no Google Colab

- Link: https://colab.research.google.com/drive/1u9vl3JIQEBJSHlo_-mtLHG4w6PMORGY_?usp=sharing

2. Execute todas as células em ordem
3. Os dados serão carregados automaticamente via URL

## Vídeo

Link do vídeo de apresentação: [INSERIR LINK AQUI]

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
