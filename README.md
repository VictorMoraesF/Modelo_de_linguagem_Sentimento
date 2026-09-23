# Modelo_de_linguagem_Sentimento
Com base em comentarios na internet idenficar o sentimento da pessoa do perfil.

# Análise de Sentimentos em Comentários Esportivos ⚽📊

# 📝 Descrição do Projeto

Este projeto tem como objetivo classificar automaticamente o sentimento (Positivo ou Negativo) de comentários orgânicos em textos na web, com forte presença de vocabulário esportivo e gírias da internet. Para isso, foi construído um pipeline de Processamento de Linguagem Natural (NLP) e Machine Learning utilizando Python.

O modelo é capaz de ler milhares de frases de torcedores ou usuários e extrair a polaridade daquela opinião, facilitando a análise de engajamento e a percepção do público sobre times, jogadores, diretoria ou eventos.

# 🛠️ Tecnologias Utilizadas

Python 3

Pandas: Manipulação e análise de dados.

NLTK: Processamento de Linguagem Natural (Tokenização e Stop Words).

Scikit-learn (sklearn): Vetorização (TF-IDF), divisão de dados, treinamento do modelo (Regressão Logística) e métricas de avaliação.

Matplotlib: Visualização de dados.

Expressões Regulares (Regex): Limpeza pesada de texto.

# ⚙️ Pipeline de Dados e Modelagem

Pré-processamento de Texto:

Conversão para minúsculas.

Remoção de pontuação e caracteres numéricos usando Regex.

Tokenização das palavras.

Remoção de Stop Words padrão do português e Stop Words personalizadas com gírias da internet (ex: 'q', 'vc', 'pra', 'mt').

Extração de Features:

Utilização do TF-IDF Vectorizer (limitado às 5000 palavras mais frequentes) para transformar texto em representações numéricas, dando peso às palavras mais relevantes.

Treinamento do Modelo:

Os sentimentos foram encodados para 0 e 1 usando LabelEncoder.

O algoritmo escolhido foi a Regressão Logística (Logistic Regression), treinado com 80% dos dados.

Avaliação:

O modelo foi testado com os 20% restantes dos dados, atingindo uma Acurácia de 75%.

Foram geradas também a Matriz de Confusão e o Relatório de Classificação (Precision, Recall e F1-Score).

# 🚀 Como Executar o Projeto

Clone este repositório.

Certifique-se de ter as bibliotecas necessárias instaladas:

pip install pandas scikit-learn matplotlib nltk


Baixe os pacotes do NLTK necessários (rode dentro do Python):

import nltk
nltk.download('stopwords')
nltk.download('punkt')


Coloque o arquivo dados_sentimentos_organicos.csv no mesmo diretório do notebook.

Execute as células do Jupyter Notebook para ver o passo a passo da limpeza, treinamento e as predições finais.

# 📈 Resultados e Conclusão

O modelo base conseguiu distinguir de forma satisfatória os comentários. Palavras como "deus", "craque", "amassou" frequentemente impulsionam classificações positivas, enquanto "bagre", "lixo", "vergonha" e "podre" associam-se a críticas negativas. O projeto serve como uma excelente base para aplicações de escuta social (social listening) no esporte.
