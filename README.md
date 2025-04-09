# Análise de Sentimentos de Reviews de Smartphone

Este projeto realiza análise de sentimentos em reviews de smartphone usando um classificador Naive Bayes. O objetivo é classificar os reviews como positivos ou negativos.

## 1. Visão Geral

O código Python fornecido realiza as seguintes etapas:

1.  **Carrega o dataset:** Carrega os reviews de um arquivo CSV.

2.  **Pré-processamento:**

    * Converte o texto para minúsculas.

    * Tokeniza o texto em palavras.

    * Remove stopwords (palavras comuns como "e", "o", "a", etc.) em português.

    * Remove caracteres não alfanuméricos.

    * Lematiza as palavras (reduz as palavras à sua forma base).

3.  **Cria o dataset de treino:**

    * Define rótulos de sentimento para cada review (positivo ou negativo).

    * Cria um conjunto de dados de treino onde cada review é representado como um dicionário de features (presença de cada palavra) e seu rótulo de sentimento.

4.  **Treina o classificador:** Treina um classificador Naive Bayes usando o conjunto de dados de treino.

5.  **Testa o classificador:**

    * Classifica os reviews originais do dataset e imprime o sentimento predito para cada um.

    * Classifica algumas frases novas de teste e imprime o sentimento predito.

## 2. Estrutura do Código

O código está organizado da seguinte forma:

* **Bibliotecas:**

    * `pandas`: Para carregar e manipular os dados.

    * `nltk`: Para processamento de linguagem natural (remoção de stopwords, lematização, tokenização) e classificação Naive Bayes.

* **Funções:**

    * `preprocessar_texto(texto)`: Realiza o pré-processamento do texto.

    * `get_features(palavras)`: Converte uma lista de palavras em um dicionário de features.

* **Variáveis:**

    * `df`: DataFrame do pandas contendo os dados do review.

    * `reviews`: Lista de reviews extraídos do DataFrame.

    * `stop_words`: Conjunto de stopwords em português.

    * `lemmatizer`: Objeto WordNetLemmatizer para lematização.

    * `reviews_processadas`: Lista de reviews pré-processados.

    * `sentimentos`: Lista de rótulos de sentimento (True para positivo, False para negativo).

    * `training_set`: Conjunto de dados de treino para o classificador.

    * `classifier`: Classificador Naive Bayes treinado.

    * `frases`: Lista de frases de teste para classificação.

## 3. Como Usar

Para executar o código, você precisa ter o Python instalado, bem como as bibliotecas `pandas` e `nltk`. Você também precisa baixar as stopwords em português do NLTK e o WordNetLemmatizer.

1.  **Instale as bibliotecas:**

    ```bash
    pip install pandas nltk
    ```

2.  **Baixe os recursos do NLTK:**

    ```python
    import nltk
    nltk.download('stopwords')
    nltk.download('wordnet')
    nltk.download('punkt')
    ```

3.  **Execute o código Python.** Certifique-se de que o arquivo `reviews_smartphone.csv` esteja no mesmo diretório do script ou especifique o caminho correto para o arquivo.

O código imprimirá o seguinte:

* Uma lista dos reviews originais.

* Uma lista dos reviews após o pré-processamento.

* O conjunto de dados de treino.

* O sentimento predito para cada review original.

* O sentimento predito para cada frase de teste.

## 4. Resultados

O código demonstra como realizar a análise de sentimentos em textos em português usando um classificador Naive Bayes. Os resultados mostram que o classificador é capaz de classificar razoavelmente bem os reviews como positivos ou negativos.

## 5. Próximos Passos

Possíveis melhorias e próximos passos incluem:

* Usar um conjunto de dados maior e mais diversificado para treinar o classificador.

* Explorar diferentes técnicas de pré-processamento de texto, como stemming ou TF-IDF.

* Experimentar com outros algoritmos de classificação, como SVM ou regressão logística.

* Avaliar o desempenho do classificador usando métricas como precisão, recall e F1-score.

* Implementar validação cruzada para avaliar a generalização do modelo.

* Criar uma interface de usuário para facilitar a entrada de texto e a visualização dos resultados.

* Adicionar mais testes e tratamento de erros.

* Otimizar o código para melhor desempenho.
