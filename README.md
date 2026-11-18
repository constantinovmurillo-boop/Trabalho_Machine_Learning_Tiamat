<img width="974" height="134" alt="651004942-0a53a0bf-93ba-4ff5-a853-cf0914d6eb95" src="https://github.com/user-attachments/assets/ee4bb882-d65b-4155-a880-60abb77464b0" />

# Projeto de Aprendizado de Máquina
Trabalho de Aprendizado de Máquina - Tiamat

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
Os dados escolhidos para ser trabalhados foram do dataset "Superconductivty Data", no qual cada linha é um material supercondutor diferente. Esse dataset, quando baixado, vem em um arquivo do tipo "ZIP", que contém um grupo de dados com propriedades físicas e químicas dos materias, chamado "train.csv", e um contendo o nome do composto e os elementos presentes nele, chamado "unique_m.csv"; ambos são do tipo "CSV". O arquivo que será usado nos algoritmos será o primeiro, contendo as propriedades dos materiais. Esse dataset foi encontrado no repositório UCI, com dados de 21.263 supercondutores, e os dados originais vêm do banco público SuperCon do NIMS. Os dados são númericos e o único dado categórico é o nome dos compostos que fica separado das propriedades que serão usadas nos algoritmos regressores. Esse dataset não contém dados faltantes, informação presente na própria página do UCI.

## Resultados
<!--ts-->
O resultado do projeto foi um modelo de floresta aleatória, com um desempenho relativamente bom, dado ao seu baixo erra medido pela raiz do erro quadrático médio. Além disso, foram estudados e desenvolvidos diversos modelos e ferramentas de aprendizado de máquina, que se apresentam úteis para situações diversas.

## Conclusão
<!--ts-->
O trabalho desenvolveu como algoritmo final de melhor desempenho um modelo de floresta aleatória que não usa PCA, possui 96 árvores, com profundidade máxima de 56, mínimo de exemplos para o split igual a 3, número mínimo de exemplos por folha sendo 1, e número máximo de atributos igual a 0.37; comi isso, o RMSE de validação foi de 9.389K.

Os principais aprendizados foram a identificação e o tratamento de dados redundantes e quase redundantes, com o uso do método de agrupamento, evitando o vazamento de dados; o uso e comparação de diferentes modelos, tal qual o modo com que operam, seu hiperparâmetros, influência da normalização e do uso de PCA para redução de dimensionalidade, dentre outros aspectos envolvendo os diferentes modelos usados; o uso do Optuna para a otimização dos modelos e intervalos de teste de hiperparâmetros; o uso de PCA para a redução de dimensionalidade e otimização dos modelos, tal qual seu controle pelo Optuna; divisão em dados de treino, teste e validação para avaliar modelos; método de validação cruzada para comparar os modelos; e a importância de explicar um modelo.

## Agradecimentos
<!--ts-->
Agradeço ao professor docente Dr. Daniel R. Cassar, por lecionar as aulas das matérias de Aprendizado de Máquina e Estatística na Ilum, Escola de Ciência. 
Agradeço também aos alunos Camila Cunha Pangrassio, Gabriela Oliveira de Lima Cabral e Arthur Cunha Rangel de Sousa por compartilharam materiais sobre os conteúdos que permitiram a realização do projeto.

## Referências
<!--ts-->
[1] HAMIDIEH, Kam. Superconductivty Data [conjunto de dados]. Irvine: UCI Machine Learning Repository, 2018. Disponível em: https://archive.ics.uci.edu/dataset/464/superconductivty+data. Acesso em: 21 set. 2026.

[2] CASSAR, Daniel R. ATP-203 1.1 - Tratamento de dados com pandas. 2026. Jupyter Notebook. Material didático não publicado.

[3] CASSAR, Daniel R. ATP-203 2.1 - Aprendizado de máquina: k-NN e métricas. 2026. Jupyter Notebook. Material didático não publicado.

[4] CASSAR, Daniel R. ATP-203 2.2 - Divisão de dados em treino e teste. 2026. Jupyter Notebook. Material didático não publicado.

[5] CASSAR, Daniel R. ATP-203 3.0 - Modelo linear e baseline. 2026. Jupyter Notebook. Material didático não publicado.

[6] CASSAR, Daniel R. ATP-203 4.0 - Árvore de decisão e floresta aleatória. 2026. Jupyter Notebook. Material d6idático não publicado.

[7] CASSAR, Daniel R. ATP-203 6.0 - Validação cruzada e otimização de hiperparâmetros. 2026. Jupyter Notebook. Material didático não publicado.

[8] CASSAR, Daniel R. ATP-203 6.1 - Vazamento de dados. 2026. Jupyter Notebook. Material didático não publicado.

[9] CASSAR, Daniel R. ATP-203 7.0 - Dados sintéticos e pipeline. 2026. Jupyter Notebook. Material didático não publicado.

[10] CASSAR, Daniel R. ATP-203 7.1 - Otimização de hiperparâmetros com optuna. 2026. Jupyter Notebook. Material didático não publicado.

[11] CASSAR, Daniel R. ATP-203 8.0 - Redução de dimensionalidade com PCA. 2026. Jupyter Notebook. Material didático não publicado.

[12] CASSAR, Daniel R. ATP-203 8.1 - Seleção de atributos. 2026. Jupyter Notebook. Material didático não publicado.

[13] SCIKIT-LEARN. Documentação do scikit-learn. Disponível em: https://scikit-learn.org/stable/. Acesso em: 15 out. 2026.

[14] OPTUNA. Documentação do Optuna. Disponível em: https://optuna.readthedocs.io/en/stable/. Acesso em: 30 out. 2026.

## Docente responsável
<!--ts-->
| <img loading="lazy" src="https://github.com/user-attachments/assets/17dfa7bf-5ca9-42df-b63e-917827fc6308" width=115><br><sub> [Prof. Dr. Daneiel Roberto Cassar](http://lattes.cnpq.br/1717397276752482) |
| :--: |

## Desenvolvedor
<!--ts-->
Murillo Constantinov, estudante do segundo semestre do bacharelado em Ciência e Tecnologia da Ilum escola de ciência.

<img width="966" height="95" alt="image" src="https://github.com/user-attachments/assets/f9825ded-4549-4691-a6e0-e261bfeb7aa1" />

