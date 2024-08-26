# Classificação Automática de Imagens de Roupas

## Visão Geral

Este projeto tem como objetivo criar um modelo de aprendizado de máquina para classificar automaticamente imagens de roupas em diferentes categorias. Utilizamos uma rede neural para processar e classificar as imagens com base em um conjunto de dados rotulado.

## Objetivos

1. *Desenvolver um modelo de classificação de imagens* que possa identificar e classificar tipos de roupas.
2. *Avaliar o desempenho do modelo* em termos de acurácia e perda durante o treinamento e validação.

## Análise dos Dados

- *Dados de Treinamento e Teste*:
  - Os dados consistem em imagens de roupas, cada uma rotulada com uma categoria específica.
  - As imagens foram divididas em conjuntos de treinamento e teste, sendo que algumas tuplas de dados foram mantidas fixas para validação.

- *Categorias de Roupas*:
  - Cada número na rotulagem corresponde a uma categoria de roupa, como: Camisa, Calça, Jaqueta, etc.

## Implementação do Modelo

1. *Definição do Modelo*:
   - *Camadas*:
     - Flatten: Achata as imagens de 28x28 pixels para uma única dimensão.
     - Dense (256 unidades): Camada densa com função de ativação ReLU para capturar relações não lineares.
     - Dense (10 unidades): Camada de saída com função de ativação Softmax para prever a probabilidade de cada classe.

2. *Compilação do Modelo*:
   - *Otimizador*: Adam
   - *Função de Perda*: sparse_categorical_crossentropy
   - *Métricas*: Acurácia

3. *Treinamento do Modelo*:
   - O modelo foi treinado por 10 épocas, usando uma fração dos dados para validação.

4. *Normalização das Imagens*:
   - As imagens foram normalizadas para ter valores entre 0 e 1, dividindo cada pixel por 255.

5. *Ajustes no Modelo*:
   - Adicionamos camadas adicionais para melhorar a performance, mas isso levou a um aumento no tempo de processamento e não melhorou o modelo. Portanto, optou-se por utilizar o modelo com menos camadas.

## Avaliação do Modelo

- *Resultados de Teste*:
  - O modelo foi avaliado usando um conjunto de teste e produziu previsões consistentes com as categorias esperadas.

- *Visualização dos Resultados*:
  - Gráficos foram gerados para mostrar a acurácia e a perda do modelo ao longo das épocas de treinamento.
