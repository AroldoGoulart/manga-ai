# README - Modelo de IA para Classificação de Mangas, Manhua, Webcomic e Novels

Este repositório contém um modelo de inteligência artificial (IA) desenvolvido para classificar imagens em quatro categorias diferentes: manga, manhua, webcomic e novel. O modelo foi treinado usando TensorFlow e Keras e utiliza uma arquitetura de rede neural convolucional (CNN) para realizar a classificação.

## Dados

O conjunto de dados utilizado para treinar e validar o modelo consiste em um total de 918 imagens distribuídas nas quatro classes da seguinte forma:

- Manga: 122 imagens
- Manhua: 579 imagens
- Webcomic: 102 imagens
- Novel: 115 imagens

As imagens foram divididas em conjuntos de treinamento e validação da seguinte maneira:

- Treinamento: 735 imagens
- Validação: 183 imagens

## Arquitetura da Rede Neural

O modelo de IA utiliza a seguinte arquitetura de rede neural:

- Normalização das imagens para o intervalo [0, 1].
- Três camadas de convolução com ativação ReLU e MaxPooling para extrair características das imagens.
- Uma camada de regularização com dropout para evitar overfitting.
- Uma camada Flatten para preparar a entrada para a rede neural densa.
- Uma camada densa com 256 neurônios e ativação ReLU.
- Uma camada de saída com ativação softmax para realizar a classificação em quatro classes.

## Treinamento do Modelo

O modelo foi treinado ao longo de 9 épocas (epochs) usando o conjunto de treinamento. Durante o treinamento, os seguintes resultados foram obtidos:

| Época | Loss (Treinamento) | Acurácia (Treinamento) | Loss (Validação) | Acurácia (Validação) |
| ----- | ------------------ | ---------------------- | ---------------- | -------------------- |
| 1/9   | 12.0615            | 0.5156                 | 0.7735           | 0.6940               |
| 2/9   | 0.5287             | 0.8286                 | 0.3873           | 0.8743               |
| 3/9   | 0.1913             | 0.9306                 | 0.2273           | 0.9235               |
| 4/9   | 0.0833             | 0.9714                 | 0.1329           | 0.9563               |
| 5/9   | 0.0291             | 0.9918                 | 0.1581           | 0.9617               |
| 6/9   | 0.0217             | 0.9946                 | 0.1486           | 0.9563               |
| 7/9   | 0.0108             | 0.9986                 | 0.1306           | 0.9617               |
| 8/9   | 0.0016             | 1.0000                 | 0.1289           | 0.9727               |
| 9/9   | 0.0005             | 1.0000                 | 0.1530           | 0.9617               |

### Gráficos de Treinamento

Aqui estão os gráficos que mostram o desempenho do modelo ao longo do treinamento:

![Training Metrics](https://i.ibb.co/CWRQPjb/image-acurracy.png)

- O gráfico superior mostra a evolução das perdas (Loss) no treinamento (linha contínua) e na validação (linha tracejada) ao longo das épocas.
- O gráfico inferior mostra a evolução das acurácias no treinamento (linha contínua) e na validação (linha tracejada) ao longo das épocas.

## Exemplo de Previsão

Aqui está um exemplo de previsão usando o modelo treinado:

![Exemplo de Previsão](https://i.ibb.co/gFc67dv/abc.png)

## Uso do Código

Para executar o código deste projeto, você precisará instalar as seguintes bibliotecas e pacotes em seu ambiente de desenvolvimento:

1. **TensorFlow**: O TensorFlow é uma das principais bibliotecas de aprendizado de máquina e deep learning. Você pode instalá-lo via pip:

   ```
   pip install tensorflow
   ```

2. **Keras**: Keras é uma API de alto nível que roda em cima do TensorFlow e facilita a construção de modelos de deep learning. Ele geralmente já está incluído na instalação do TensorFlow.

3. **Matplotlib**: A biblioteca Matplotlib é usada para criar gráficos e visualizações dos resultados do treinamento. Instale-a com:

   ```
   pip install matplotlib
   ```

4. **NumPy**: NumPy é uma biblioteca para computação numérica em Python e é usada para manipular os dados das imagens. Instale-o com:

   ```
   pip install numpy
   ```

Certifique-se de que você tenha um ambiente Python configurado corretamente para a execução deste projeto. Recomenda-se o uso de um ambiente virtual para isolar as dependências.

Após instalar as bibliotecas, você pode executar o código presente no repositório para criar, treinar e avaliar o modelo de IA. Certifique-se de ajustar os caminhos dos diretórios de acordo com a localização dos seus dados.
