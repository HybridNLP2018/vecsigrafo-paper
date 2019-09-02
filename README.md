# Additional material for "Vecsigrafo: Corpus-based Word-Concept Embeddings"

This repo contains additional material for the paper, which has been published at the [Semantic Web Journal](http://semantic-web-journal.net/content/vecsigrafo-corpus-based-word-concept-embeddings-bridging-statistic-symbolic-1).

# Evaluation Results

Test result data for "Vecsigrafo: Corpus-based Word-Concept Embeddings"

## Word-similarity ablation study
As part of evaluating Vecsigrafo, we studied how variations to Vecsigrafo-based embeddings affect the quality of the lexical and semantic embeddings. We did this by analyzing the various results using word-similarity tasks,  which  we  extend  to  also  take  into  account concept-similarity. We provide a [tsv file with results](https://github.com/HybridNLP2018/vecsigrafo-paper/blob/master/vecsigrafo-ablation-study-wordsim-20180816.tsv).

The fields in the tsv file are:
  * `dataset`: the name of the word similarity dataset
  * `embA`: the path to the 'A' embedding
  * `evalTypeA`: word-based (the standard way: use words from the embedding vocabulary to calculate a cosine similarity to compare to the human similarity metric) or concept-based (find all concepts matching the word pairs in the dataset and select the concept pair that has the highest similarity)
  * `embB`: the path to the 'B' embedding. if 'na', the correlation results are those from embA against the dataset. When not 'na', the correlation results refer to the correlation between the similarity as predicted by embA and embB.
  * `evalTypeB`: word-based or concept-based (see evalTypeA)
  * `rho`: spearman correlations score
  * `pearsons`: correlation score
  * `rho_pairs`: number of pairs used to calculate the correlation scores (this will be smaller or equal to the number of pairs in the dataset, as some words may be missing from the embedding vocabularies).
  * `ds_pairs`: number of pairs available in the dataset

# Tutorial on Vecsigrafo

We presented a [tutorial on Vecsigrafo and related technologies at ISWC 2018](http://expertsystemlab.com/hybridNLP18/). The materials for the tutorial are based on executable Jupyter notebooks available from the [tutorial repo](https://github.com/HybridNLP2018/tutorial) and can be executed from [Google Colaboratory](https://colab.research.google.com).
