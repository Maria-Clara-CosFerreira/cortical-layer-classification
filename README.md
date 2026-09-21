<img width="2535" height="380" alt="image" src="https://github.com/user-attachments/assets/812330bb-3fba-4591-8ce5-75e266dd1a03" />
# Classificação de Regiões Cerebrais com KNN

## Projeto Final da Disciplina de Prática em Ciência de Dados

Instituição de ensino vinculada à desenvolvedora do projeto: Ilum Escola de Ciência - CNPEM (Centro Nacional de Pesquisa em Energia e Materiais)

## Autora

Maria Clara Costa Ferreira

## Descrição do projeto

Este projeto consiste na aplicação do algoritmo de aprendizado de máquina *K-Nearest Neighbors (KNN)* para a classificação de neurônios de acordo com sua estrutura cerebral, utilizando dados experimentais disponibilizados pelo *Allen Institute* no dataset Cell Types Specimen.

O modelo utiliza principalmente características eletrofisiológicas dos neurônios, além da espécie do organismo, para tentar prever a estrutura cerebral à qual cada célula pertence. O alvo da classificação é o atributo structure__acronym, que identifica a região cerebral e, quando aplicável, a camada cortical correspondente.

Para avaliar e otimizar o modelo, foram testadas diferentes combinações de hiperparâmetros do KNN utilizando *validação cruzada* e *GridSearchCV*. Também foi analisado o efeito da normalização dos atributos numéricos sobre o desempenho do algoritmo.

Além da avaliação por métricas de classificação e matriz de confusão, as previsões do modelo foram utilizadas em uma *visualização tridimensional do cérebro* com a biblioteca Brainrender. Dessa forma, é possível comparar a localização real dos neurônios com a localização prevista pelo modelo.

## Organização do repositório

### Notebook principal

* criatura_lendaria1.ipynb

O notebook contém toda a implementação do projeto, incluindo:

* Introdução teórica sobre classificação de neurônios e KNN;
* Carregamento e organização dos dados do Allen Institute;
* Seleção das classes utilizadas na classificação;
* Separação dos dados em conjuntos de treino e teste;
* Pré-processamento dos atributos numéricos e categóricos;
* Comparação entre dados normalizados e não normalizados;
* Construção do modelo KNN;
* Otimização de hiperparâmetros por meio de GridSearchCV;
* Validação cruzada;
* Avaliação do modelo utilizando acurácia e balanced accuracy;
* Construção da matriz de confusão;
* Análise gráfica dos resultados;
* Visualização tridimensional das regiões cerebrais e dos neurônios utilizando Brainrender.

## Dataset

Foi utilizado o dataset *Cell Types Specimen*, disponibilizado pelo Allen Institute, contendo informações experimentais de neurônios de diferentes espécies, incluindo características eletrofisiológicas e informações sobre sua localização anatômica.

As classes utilizadas no projeto correspondem a diferentes estruturas cerebrais representadas pelo atributo structure__acronym.

## Como executar

1. Abra o notebook criatura_lendaria1.ipynb.
2. Execute as células na ordem em que aparecem.
3. Certifique-se de que o dataset utilizado pelo projeto esteja disponível no ambiente de execução.
4. Execute as etapas de preparação dos dados e treinamento do modelo.
5. Ao final, observe as métricas, gráficos, matriz de confusão e visualizações tridimensionais geradas pelo projeto.

## Bibliotecas utilizadas

* pandas — organização, manipulação e análise dos dados;
* NumPy — operações numéricas e manipulação de arrays;
* scikit-learn — pré-processamento, treinamento do KNN, validação cruzada, otimização de hiperparâmetros e avaliação do modelo;
* seaborn — criação de visualizações estatísticas e mapas de calor;
* matplotlib — criação e personalização dos gráficos;
* Brainrender — visualização tridimensional do cérebro e de suas estruturas;
* vedo — suporte à renderização e visualização tridimensional;
* random — seleção aleatória de neurônios para a visualização.
