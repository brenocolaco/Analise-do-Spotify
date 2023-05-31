# Analise-do-Spotify

# Resumo
Uma análise de dados proposta pela ALURA para o #7DaysOfCode com o objetivo de abordar os métodos, ferramentas e análises de Machine Learning.

# Sobre o Projeto

O Projeto foi dividido sobre a seguinte abordagem

- [Coleta de Dados e Análise Exploratória](#coleta-de-dados-e-análise-exploratória)
- [Conceitos de Machine Learning e Pré-Processamento de Dados](#conceitos-de-machine-learning-e-pré-processamento-de-dados)
- [Divisão dos Dados e Validação Cruzada](#divisão-dos-dados-e-validação-cruzada)
- [Baseline e 1º Modelo](#baseline-e-1º-modelo)
- [Validação do Modelo](#validação-do-modelo)

## Coleta de Dados e Análise Exploratória 

<p>A análise exploratória é o primeiro passo para ter um entendimento dos dados para identificar padrões, tendências e relações entre as variáveis.</p>
<p>Nesse primeiro momento é onde criamos perguntas e tentamos responde-las com o passar do projeto. O dicionário dos dados, também, é de suma importância para o entendimento.</p>
<p>Os dados foram baixados do <a href="https://www.kaggle.com/">Kaggle</a> e depois importados através do proprio Github e para as análises iniciais foram utilizadas as bibliotecas do <a href="https://pandas.pydata.org/">Pandas</a> e <a href="https://matplotlib.org/">Matplotlib</a> para visualização.</p>

## Conceitos de Machine Learning e Pré-Processamento de Dados

<p>Existem três tipos principais de machine learning (aprendizado de máquina): supervisionado, não supervisionado e por reforço. Neste projeto o caso estudado foi um aprendizado supervisionado para um modelo de classificação. O intuito, então, foi criar um modelo para dizer se uma música será popular ou não. </p>
<p>Antes de criar o modelo, porém, foi realizado o pré-processamento dos dados: remoção de dados ausentes, remoção de dados duplicados, normalização dos dados e criação de classes de popularidade, uma vez que, de acordo com a documentação da API do Spotify a popularidade varia numa escala de 0 a 100. Esse número é baseado no número total de reproduções que a faixa teve e quão recentes são as reproduções.</p> 

## Divisão dos Dados e Validação Cruzada

<p>Após o pré-processamento foi feita a divisão dos dados. Inicialmente, a divisão foi feita de forma aleatória mas por existir um desbalanceamento dos dados notou-se que essa não era a estratégia mais adequada. Então, foi feita a validação cruzada, que é usada para avaliar a capacidade de generalização do modelo em diferentes conjuntos de dados. Nessa etapa foi usada a biblioteca do <a href="https://scikit-learn.org/stable/">Scikit-Learn</a> tanto para divisão aleatoria quanto para a validação cruzada.</p>

## Baseline e 1º Modelo

<p>A baseline, como o nome ja sugere, é a nossa linha base. Foi feito uma baseline pelo DummyClassifier para a divisão aleatória e para a validação cruzada foi adotada como baseline a Regressão Logística. A Regressão Logística é frequentemente usada como um modelo de baseline em problemas de classificação, por ser um modelo simples e fácil de interpretar.<p>
  
## Validação do Modelo
  
<p>A etapa de validação é crucial para o projeto. Ao utilizar as metricas adequadas definimos a qualidade do modelo e avaliamos se ele atende aos requisitos propostos. A avaliação de um modelo de classificação é feita a partir da comparação entre as classes preditas pelo modelo e as classes verdadeiras de cada exemplo. Todas as métricas tem o objetivo de medir quão distante o modelo está de uma classificação perfeita mas cada uma de uma forma diferente</p>
