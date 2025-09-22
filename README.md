# Análise de Performance de Estudantes

Este projeto realiza uma análise preditiva da performance de estudantes utilizando técnicas de Machine Learning, com foco especial na identificação de problemas comuns em datasets do mundo real.

##  Objetivo

Desenvolver um modelo de regressão linear para prever o índice de performance de estudantes com base em variáveis como horas de estudo, notas anteriores, atividades extracurriculares, horas de sono e prática com questões de exemplo.


## Dataset

### Variáveis do Dataset:
- **Hours Studied**: Horas de estudo
- **Previous Scores**: Notas anteriores do estudante
- **Extracurricular Activities**: Participação em atividades extracurriculares (Sim/Não)
- **Sleep Hours**: Horas de sono
- **Sample Question Papers Practiced**: Quantidade de questões de exemplo praticadas
- **Performance Index**: Índice de performance (variável alvo)

### Características dos Dados:
- **Linhas**: ~10.000 estudantes
- **Tipo**: Dados tabulares com variáveis numéricas e categóricas
- **Fonte**: Kaggle

## Tecnologias Utilizadas

- **Python 3.13+**
- **Pandas**: Manipulação de dados
- **NumPy**: Computação numérica
- **Scikit-learn**: Machine Learning
- **Seaborn/Matplotlib**: Visualização
- **Jupyter Notebook**: Ambiente de desenvolvimento

## 🛠️ Metodologia

### 1. Análise Exploratória
- Limpeza e formatação dos dados
- Conversão de variáveis categóricas para numéricas
- Análise de correlações entre variáveis
- Identificação de outliers

### 2. Pré-processamento
- Padronização de variáveis com StandardScaler
- Divisão treino/teste (80/20)
- Tratamento de variáveis categóricas

### 3. Modelagem
- **Algoritmo**: Regressão Linear
- **Métricas de Avaliação**:
  - Mean Absolute Error (MAE)
  - Mean Squared Error (MSE)
  - Root Mean Squared Error (RMSE)
  - R² Score

### 4. Predições
- Aplicação do modelo em dados de teste
- Geração de previsões para novos estudantes

## Resultados

### Métricas do Modelo:
- **Mean Absolute Error**: 1.62
- **Mean Squared Error**: 4.16
- **Root Mean Squared Error**: 2.04
- **R² Score**: 0.989

### Análise de Correlações:
A análise revelou que a variável `Previous Scores` possui correlação extremamente alta com a variável alvo, enquanto outras variáveis apresentam correlações muito baixas.

## Limitações e Problemas Identificados

### 1. **Data Leakage**
- A variável `Previous Scores` domina completamente o modelo
- Usar notas passadas para prever performance futura pode ser considerado vazamento de dados
- O R² de 0.989 é artificialmente alto devido a essa dependência

### 2. **Baixa Correlação de Outras Variáveis**
- Variáveis como `hours_studied`, `sleep_hours` têm correlação quase zero com a performance
- Isso contradiz a intuição de que horas de estudo deveriam impactar o desempenho

### 3. **Utilidade Prática Limitada**
- Na prática, seria mais útil prever performance baseado em fatores controláveis
- O modelo atual oferece pouco insight para melhorar o desempenho estudantil

## Como Executar

1. Baixe todos os arquivos do repositório.
2. Abra os notebooks na ordem das etapas, em qualquer ambiente que suporte .ipynb (os notebooks foram escritos no Jupyter através do Anaconda)
3. Execute as células sequencialmente (Shift + Enter)



## 📝 Conclusão

Este foi um projeto entry-level cujo intuito era, necessariamente, trabalhar com um dataset simples. Contudo, a escolha de um dataset simples não compreendia todas as expectativas acerca das possibilidades disponíveis; a intenção era conseguir construir modelos diferentes e comparar as performances. Entretanto, após constatar a natureza da correlação entre as variáveis, tomei a decisão de aceitar a performance de 98% com o modelo mais simples.

Embora o modelo apresente métricas estatisticamente excelentes, a análise revela limitações importantes que comprometem sua aplicabilidade prática. Este projeto demonstra a importância de uma análise crítica dos dados e resultados, indo além das métricas numéricas para avaliar a validade e a utilidade real do modelo.

No que diz respeito aos aprendizados, o projeto serviu como uma experiência sólida no que tange à análise exploratória e à aplicação das técnicas. Porém, talvez o aspecto mais importante tenha sido o pensamento crítico para identificar problemas em datasets reais, a necessidade de validar a lógica de negócio por trás dos dados (não adianta criar um modelo preditor que basicamente só leva em conta o histórico anterior dos alunos) e a percepção de que métricas aparentemente boas podem mascarar problemas fundamentais.

---

*Projeto desenvolvido como parte de estudos em Data Science e Machine Learning.*
## 👨‍💻 Autor
**Vitor Fernandes**  
[LinkedIn](https://www.linkedin.com/in/vitor-fernandes-s/)  
Email: vitorbfernandes.s@gmail.com

