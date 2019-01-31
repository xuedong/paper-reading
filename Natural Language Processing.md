# Natural Language Processing

## Summary

* [Linguistics](#linguistics)
* [Speech Recognition](#speech-recognition)
* [Natural Language Processing](#natural-language-processing)
* [Natural Language Understanding](#natural-language-understanding)

## Papers

### Linguistics

### Speech Recognition

### Natural Language Processing

#### Word Embeddings

* **`word2vec`** [Efficient Estimation of Word Representations in Vector Space](https://arxiv.org/abs/1301.3781), T. Mikolov et al., 2013.
	- Two neural network based architectures are proposed to learn distributed word representations: skip-gram and CBOW.
* **`NEG`** [Distributed Representations of Words and Phrasesand their Compositionality](https://arxiv.org/abs/1310.4546), T. Mikolov et al., 2013.
	- This is an incremental work on top of the original word2vec paper.
	- The authors use NEG, which is a light version of NCE to define the conditional probability model of contexts.
	- Subsampling is used to speedup the training, and it can also slightly improve the accuracy.
	- Phrase representations can also be done in the same fashion.
* **`GloVe`** [GloVe: Global Vectors for Word Representation](https://nlp.stanford.edu/pubs/glove.pdf), J. Pennington et al., 2014.

### Natural Language Understanding

