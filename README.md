# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

Bem-vindo ao desafio de projeto "Previsão de Estoque Inteligente na AWS com SageMaker Canvas. Neste Lab DIO, você aprenderá a usar o SageMaker Canvas para criar previsões de estoque baseadas em Machine Learning (ML). Siga os passos abaixo para completar o desafio!

## 📋 Pré-requisitos

Antes de começar, certifique-se de ter uma conta na AWS. Se precisar de ajuda para criar sua conta, confira nosso repositório [AWS Cloud Quickstart](https://github.com/digitalinnovationone/aws-cloud-quickstart).


## 🚀 Passo a Passo

### 1. Selecionar Dataset

-   Foi escolhido o dataset "dataset-500-curso-sagemaker-canvas-dio.csv" que se encontra no diretório "datasets" e feito o upload deste para treinar o meu modelo de previsão de estoque.
![Captura de Tela (31)](https://github.com/user-attachments/assets/4bbfac74-cf11-4f84-b502-d8bd3240ebd1)

### 2. Construir/Treinar

-   No SageMaker Canvas, foi importado o dataset selecionado.
![Captura de Tela (32)](https://github.com/user-attachments/assets/d137ec8a-c61e-425f-870b-296f7ef45bf9)

-   Configuração de variáveis de entrada e saída definidas. Foi decidido rodar com a opção de build "Quick build" para favorecer o tempo.
![Captura de Tela (33)](https://github.com/user-attachments/assets/811f3418-ea8f-489d-9bac-85e644e1b646)

-   Treinamento do modelo iniciado e após algum tempo, seguimos para próximo passo.
![Captura de Tela (34)](https://github.com/user-attachments/assets/dbcf31fb-201c-47a7-9cab-570c5d383e9a)

### 3. Analisar

-   Examinando as métricas de performance do modelo. Quanto mais próximo os valores das métricas forem de zero, indica que o modelo tem um desempenho mais preciso.
![Captura de Tela (35)](https://github.com/user-attachments/assets/79740565-9d27-4b26-b8e3-23e781442963)

**Avg. WQL (Average Weighted Quantile Loss):** 
Essa métrica mede a precisão das previsões probabilísticas. Ela penaliza erros com base no quantil estimado, atribuindo diferentes pesos para superestimações e subestimações. Neste modelo, está muito próximo de zero, indicando que teve alta precisão.

**MAPE (Mean Absolute Percentage Error):**
O MAPE representa o erro percentual médio entre as previsões do modelo e os valores reais. Neste modelo, o MAPE é 29%, o que significa que, em média, as previsões estão a 29% de erro em relação aos valores reais.

**WAPE (Weighted Absolute Percent Error):** 
Similar ao MAPE, o WAPE considera pesos diferentes para diferentes itens com base em sua importância ou volume. Neste modelo, o WAPE é 15,2%, sugerindo um erro menor quando ponderado.

**RMSE (Root Mean Square Error):** 
O RMSE mede o desvio padrão dos erros de previsão. Quanto menor o valor, melhor. Neste modelo, o RMSE é aproximadamente 1,535, indicando a dispersão dos erros de previsão.

**MASE (Mean Absolute Scaled Error):** 
O MASE compara o erro absoluto médio do modelo com o erro absoluto médio de um modelo ingênuo (como a média móvel). Valores abaixo de 1 indicam que o modelo é melhor do que o modelo ingênuo.

### 4. Prever

-   O modelo treinado foi utilizado para fazer previsões de estoque. O dataset utilizado não permite análises de diferentes variaveis, mas permite verificar diferentes comportamentos de diferentes produtos de acordo com o tempo, tendo produtos que reduzem sua quantidade num melhor cenário enquanto outros aumentam sua quantidade ao decorrer.
