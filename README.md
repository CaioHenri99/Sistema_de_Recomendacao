# Sistema_de_Recomendacao
Este projeto é um sistema de recomendação de filmes desenvolvido em Python. Ele utiliza técnicas de **Filtragem Baseada em Conteúdo (Content-Based Filtering)** combinadas com um score de popularidade para sugerir títulos relevantes e de alta qualidade.

## 🚀 Funcionalidades

- **Base de Dados Unificada:** Integração e limpeza de múltiplos datasets de gêneros (Ação, Drama, Crime, Animação, Sci-Fi, etc.).
- **Processamento de Linguagem Natural (NLP):** Vetorização de gêneros utilizando `CountVectorizer`.
- **Similaridade de Cosseno:** Cálculo matemático para encontrar a proximidade entre filmes.
- **Lógica Híbrida:** O algoritmo não recomenda apenas o filme mais parecido, mas pondera a nota do IMDb (Rating) para garantir recomendações de qualidade.
- **Deduplicação Inteligente:** Tratamento de dados para remover filmes repetidos entre diferentes arquivos CSV.

## 🛠️ Tecnologias Utilizadas

- **Python 3**
- **Pandas** (Manipulação e fusão de dados)
- **Scikit-Learn** (CountVectorizer, Cosine Similarity)

## 📊 Como funciona a Lógica Híbrida?

O sistema calcula um *Score Final* para cada filme candidato seguindo a fórmula:

$$Score = (Similaridade \times 0.8) + (NotaNormalizada \times 0.2)$$

Isso garante que o filme recomendado seja tematicamente idêntico (80% de peso) mas também bem avaliado pela crítica/público (20% de peso).

## 📂 Estrutura do Projeto

O projeto lê arquivos CSV separados por gênero, unifica-os em um único Dataframe robusto e aplica o modelo de recomendação.

---
Desenvolvido por [Caio Henrique](https://github.com/caiohenri99)
