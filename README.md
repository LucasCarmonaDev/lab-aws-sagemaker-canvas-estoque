# 🐱‍💻 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

Este projeto tem como objetivo desenvolver um modelo de Machine Learning para prever o estoque de produtos de tecnologia com base em um conjunto de dados simulado. O projeto foi desenvolvido como parte de um bootcamp para demonstrar habilidades em ciência de dados e machine learning.

## 🚩 Descrição do Objetivo

O objetivo é prever o estoque diário de produtos com base em dados históricos simulados. O dataset utilizado por mim contém informações sobre o ID do produto, nome do produto, data do evento (dia), indicador de promoção (FLAG_PROMOCAO), e quantidade em estoque (QUANTIDADE_ESTOQUE).


## 🐍 Dataset

Por meio de um script em Pyhton gerei o dataset:
https://github.com/LucasCarmonaDev/Script-Dataset/blob/main/Script

### Observações sobre o Dataset
- Nomes dos Produtos: Os nomes dos produtos são genéricos e representam diferentes tipos de tecnologia, como smartphones, tablets, laptops, etc.
- Simulação de Dados: O dataset foi simulado para demonstrar um histórico fictício de estoque de produtos, visando a aplicação de técnicas de machine learning.



## 🚀 Passo a Passo seguido

### 1. Selecionar Dataset

-   Fiz o upload do dataset no SageMaker Canvas conforme gerado pelo script.


### 2. Construir/Treinar

-   No SageMaker Canvas, importei o dataset selecionado.
![Passo1](https://github.com/LucasCarmonaDev/lab-aws-sagemaker-canvas-estoque/assets/171631260/07bf4fa5-d09f-4d81-bc81-43c5599caace)
-   Configurei as variáveis de entrada e saída de acordo com os dados.
![EntradaSaida](https://github.com/LucasCarmonaDev/lab-aws-sagemaker-canvas-estoque/assets/171631260/0fff206e-dde4-4555-bb62-2469d537767c)
-   Iniciei o treinamento do modelo (quick).

### 3. Analisar

-   Após o treinamento, examinei as métricas de performance do modelo.
-   Verifiquei as principais características que influenciam as previsões.
![Metricas](https://github.com/LucasCarmonaDev/lab-aws-sagemaker-canvas-estoque/assets/171631260/ea1c4130-445b-4bd0-84a2-ee061e3d951d)

### 4. Prever

-   Usei o modelo treinado para fazer previsões de estoque.
-   Exportei os resultados e analisei as previsões geradas.

# ✔ Resultados

## Métricas de Avaliação do Modelo
Durante o desenvolvimento do modelo de machine learning, foram obtidas as seguintes métricas de desempenho:

- Avg. wQL (Weighted Quantile Loss): 0.259
- MAPE (Mean Absolute Percentage Error): 1.391
- WAPE (Weighted Absolute Percentage Error): 0.427
- RMSE (Root Mean Squared Error): 26.902
- MASE (Mean Absolute Scaled Error): 4.132

### Análise das Métricas
O RMSE (Root Mean Squared Error) apresentou uma variação alta devido à falta de valores futuros no dataset. Isso pode impactar a precisão das previsões, pois o modelo não possui informações sobre o comportamento futuro do estoque. É importante destacar que o objetivo principal deste projeto é demonstrar a capacidade de desenvolver e aplicar técnicas de machine learning, mesmo utilizando um dataset simulado que não reflete completamente a realidade.

## Insights a partir dos Dados
### Exemplos de Produtos Analisados
- Produto ID_1010  Data: 2025-06-17 /	P10: 6.019 / P50: 40.982 / P90: 73.257
![single_prediction_results](https://github.com/LucasCarmonaDev/lab-aws-sagemaker-canvas-estoque/assets/171631260/4357a42c-af62-49cc-9957-88cd99c104db)

- Produto ID_1011  Data: 2025-06-17 / P10: 6.989 / P50: 49.352 / P90: 77.242
![single_prediction_results (1)](https://github.com/LucasCarmonaDev/lab-aws-sagemaker-canvas-estoque/assets/171631260/6b27327d-889a-435e-91be-24082aa8a22a)

### Considerações sobre os Insights
Os insights obtidos dos percentis P10, P50 e P90 permitem uma análise detalhada do estoque diário de produtos específicos ao longo do tempo. Essas informações são cruciais para ajustes na gestão de estoque e podem orientar decisões estratégicas para evitar rupturas ou excessos de estoque. Nos exemplos é possível perceber um aumento na demanda que indica que será necessária uma reposição.

## Conclusão
Este projeto demonstra habilidades em ciência de dados e machine learning utilizando as ferramentas do Sagemaker Canvas por meio da avaliação de modelos de previsão de estoque. O uso de um dataset fictício de produtos de tecnologia permite explorar técnicas de modelagem preditiva e entender os desafios envolvidos na construção de modelos de machine learning para problemas de negócio, facilitando esse entendimento por meio de uma ferramenta que não obriga a utilização de código.


