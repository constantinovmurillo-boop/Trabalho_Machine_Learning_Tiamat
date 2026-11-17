<img width="974" height="134" alt="651004942-0a53a0bf-93ba-4ff5-a853-cf0914d6eb95" src="https://github.com/user-attachments/assets/ee4bb882-d65b-4155-a880-60abb77464b0" />

# Projeto de Aprendizado de Máquina
Trabalho de Aprendizado de Máquina - Cubo Gelatinoso

## Cabeçalho
<!--ts-->
**Aluno:** Murillo Constantinov

**RM:** 2610072

**Turma:** Turma 2026

**Disciplina:** Aprendizado de Máquina

**Docente:** professor Dr. Daniel R. Cassar

**Instituição:** Ilum - Escola de Ciência

**Local:** Campinas -  SP, Brasil

**Data:** 13/09/2026

## Contextualização
<!--ts-->
O Tiamat é a entrega final da disciplina de Aprendizado de Máquina da Ilum, Escola de Ciência. Essa tarefa tem o objetivo de os estudantes escolherem um conjunto de dados e compare o desempenho de pelo menos 3 algoritmos/pipelines de aprendizado de máquina (sem contar o baseline). É necessário testar pelo menos 100 conjuntos diferentes de hiperparâmetros para cada algoritmo/pipeline escolhido utilizando o Optuna.

## Métodologia
<!--ts-->
A metodologia envolveu baixar o banco de dados adaptando-o para ser trabalhado, em seguida ele foi estudado, com análises exploratórias e estatísticas; limpo para ser trabalhado e divididos em atributos e target, sendo transformados para as necessidades durante o projeto; para evitar vazamento de dados, foi usada a técnica de agrupamento para evitar dados redundantes ou quase redundantes. Em seguida, os dados foram separados em treino e teste e o split foi avaliado. A métrica de desempenho escolhida foi a raiz do erro quadrático médio (RMSE). Para a modelagem, foram separados dados de treino e de validação. Foi feito e avaliado um modelo Baseline para se ter uma base de desempenho; além dele foram desenvolvidos, avaliados e otimizados com o Optuna os modelos de regressão linear, regressão polinomial, k-NN, árvore de decisão e floresta aleatória. O uso do Optuna envolveu a escolha dos melhores hiperparâmetros encontrados, escolha do uso ou não de PCA para a redução de dimensionalidade e da normalização dos dados. Com os modelos pronto, eles foram avaliados pelo método de validação cruzada k-fold e os modelos foram comparados. Então, os algoritmos foram testados e avaliados no conjunto de teste e comparados para a avaliação final. Todos os processos envolveram também pesquisa, estudo e aplicação de conceitos de Aprendizado de Máquina.

### Bibliotecas utilizadas
<!--ts-->
Para organizar a realização do projeto, foram importadas as bibliotecas a seguir. A biblioteca "statistics" foi usada para fazer análise e cálculos estatísticos dos dados. A biblioteca "pandas" foi usada para a manipulação e visualização dos dados. A biblioteca "numpy" teve uso em momentos de análises estatísticas. As bibliotecas "matplotlib" e "seaborn" foram utilizadas para construções gráficas. A biblioteca "warnings" foi usada para controlar mensagens do python. Os objetos importadas da biblioteca "sklearn" e "scipy" foram usadas para diversos fins; portanto, tiveram suas funções explicados nas seções em que foram utilizados. A biblioteca "optuna" foi usada para realizar os processos envolvendo o Optuna e a otimização com ele.

### Conjunto de dados
<!--ts-->

