# WellMe - Previsão de Engajamento de Usuários Utilizando MLP

## Sobre o Projeto

O **WellMe** é uma proposta de solução digital voltada à promoção de hábitos saudáveis por meio de gamificação, desenvolvida no contexto do ecossistema da **Care Plus**.

A ideia do projeto é incentivar os usuários a realizarem atividades relacionadas ao bem-estar, como prática de exercícios físicos, movimentação diária e manutenção de hábitos saudáveis. A plataforma utiliza elementos de gamificação, incluindo desafios, metas, progressão por níveis e recompensas, buscando aumentar o engajamento dos usuários ao longo do tempo.

Este projeto foi desenvolvido com foco na aplicação de técnicas de Inteligência Artificial e Machine Learning para prever o nível de engajamento dos usuários com base em seus comportamentos diários.

---

# Objetivo

O principal objetivo do projeto é desenvolver um modelo capaz de prever o nível de engajamento dos usuários dentro do contexto do WellMe.

Para isso, foram utilizados dados relacionados a:

- número de passos;
- minutos de atividade física;
- tempo sedentário;
- calorias gastas.

A partir dessas informações, foi construída uma variável de engajamento classificada em:

- High
- Medium
- Low

O modelo treinado busca identificar padrões comportamentais que possam futuramente auxiliar na personalização da experiência dos usuários dentro da aplicação.

---

# Dataset Utilizado

O projeto utiliza como base o dataset público:

**Fitbit Fitness Tracker Data**

Disponível em:
https://www.kaggle.com/datasets/arashnic/fitbit

Como não há acesso a dados reais do WellMe, o dataset foi utilizado como referência para simular o comportamento dos usuários no contexto da aplicação.

O arquivo original do dataset não foi incluído diretamente no repositório GitHub devido ao seu tamanho. Dessa forma, para execução completa do projeto, é necessário realizar o download manual do dataset por meio do link disponibilizado acima e adicioná-lo na pasta `data/raw/`.

---

# Tecnologias Utilizadas

## Linguagem

- Python

## Bibliotecas

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

---

# Estrutura do Projeto

```bash
wellme-engagement-mlp/
│
├── data/
│   ├── raw/
│   │   └── fitbit_daily_activity.csv
│   │
│   └── processed/
│       └── fitbit_processed.csv
│
├── notebooks/
│   ├── 01_data_exploration_eda.ipynb
│   ├── 02_data_preprocessing.ipynb
│   ├── 03_mlp_model_training.ipynb
│   └── 04_final_analysis_and_insights.ipynb
│
└── README.md
```

---

# Etapas do Projeto

## 1. Exploração de Dados (EDA)

Nesta etapa, foram realizadas análises exploratórias do dataset, incluindo:

- estrutura dos dados;
- estatísticas descritivas;
- análise de distribuições;
- correlação entre variáveis;
- interpretação comportamental dos usuários.

Também foram desenvolvidos gráficos para análise de:

- passos diários;
- tempo sedentário;
- calorias gastas;
- correlação entre variáveis.

---

## 2. Pré-processamento dos Dados

Nesta etapa, foram realizadas:

- seleção das variáveis relevantes;
- criação da variável de engajamento;
- organização dos dados;
- separação entre dados brutos e processados.

A variável `Engagement` foi criada utilizando percentis do próprio dataset, considerando:

- atividade física;
- sedentarismo;
- gasto calórico.

---

## 3. Treinamento do Modelo MLP

Foi desenvolvido um modelo de rede neural do tipo **MLP (Multilayer Perceptron)** utilizando a biblioteca `scikit-learn`.

### Configurações do modelo

- duas camadas ocultas:
  - 64 neurônios
  - 32 neurônios
- função de ativação:
  - ReLU
- otimizador:
  - Adam
- normalização dos dados:
  - StandardScaler

---

# Avaliação do Modelo

O modelo foi avaliado utilizando:

- Accuracy
- Classification Report
- Matriz de Confusão
- Curva de Loss durante o treinamento

Os resultados demonstraram boa capacidade de classificação dos diferentes níveis de engajamento dos usuários.

---

# Possíveis Aplicações no WellMe

O modelo desenvolvido pode futuramente ser utilizado para:

- personalização de desafios;
- recomendação de metas;
- envio de incentivos motivacionais;
- identificação de usuários com baixo engajamento;
- adaptação dinâmica da experiência do usuário;
- apoio a estratégias de retenção e gamificação.

---

# Limitações do Projeto

Algumas limitações importantes do projeto incluem:

- utilização de dataset público em vez de dados reais do WellMe;
- variável de engajamento criada artificialmente;
- ausência de dados relacionados ao uso real da aplicação;
- conjunto limitado de variáveis comportamentais.

---

# Conclusão

O projeto demonstrou como técnicas de Inteligência Artificial e Machine Learning podem ser aplicadas no contexto de saúde e bem-estar para análise comportamental e previsão de engajamento.

Os resultados obtidos indicam que redes neurais do tipo MLP possuem potencial para apoiar futuras estratégias de personalização dentro do WellMe, contribuindo para o incentivo à adoção de hábitos saudáveis.

---

# Integrantes do Grupo

- ERICK MOLINA — RM 553852
- FELIPE CASTRO SALAZAR — RM 553464
- MARCELO VIEIRA DE MELO — RM 552953
- RAYARA AMARO FIGUEIREDO — RM 552635
- VICTOR RODRIGUES — RM 554158

---

# Disciplina

Projeto desenvolvido para o Challenge da disciplina:

**Inteligência Artificial & Machine Learning**

Professor:
**Danilo Rodrigues de Assis Elias**
