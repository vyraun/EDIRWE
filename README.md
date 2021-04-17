# Python-3 Version:

Converted original code from [https://github.com/vyraun/Half-Size](https://github.com/vyraun/Half-Size) to Python3. It works for python3.7 tested on GloVe Embeddings.

Please checkout the original GitHub Repository at [https://github.com/vyraun/Half-Size](https://github.com/vyraun/Half-Size)

## Original README.md
Code for [Effective Dimensionality Reduction for Word Embeddings](https://www.aclweb.org/anthology/W19-4328/), and its earlier [version](https://arxiv.org/abs/1708.03629).

Accepted at NIPS 2017 LLLD Workshop and Published at the 4th Workshop on Representation Learning for NLP, ACL.

> Abstract: Word embeddings have become the basic building blocks for several natural language processing and information retrieval tasks. Pre-trained word embeddings are used in several downstream applications as well as for constructing representations for sentences, paragraphs and documents. Recently, there has been an emphasis on further improving the pre-trained word vectors through post-processing algorithms. One such area of improvement is the dimensionality reduction of the word embeddings. Reducing the size of word embeddings through dimensionality reduction can improve their utility in memory constrained devices, benefiting several real-world applications. In this work, we present a novel algorithm that effectively combines PCA based dimensionality reduction with a recently proposed post-processing algorithm, to construct word embeddings of lower dimensions. Empirical evaluations on 12 standard word similarity benchmarks show that our algorithm reduces the embedding dimensionality by 50%, while achieving similar or (more often) better performance than the higher dimension embeddings.

The word-vector evaluation code is directly used from https://github.com/mfaruqui/eval-word-vectors.

Run the script ```algo.py``` (embedding file location is hardcoded as of now) to reproduce the algorithm and its evaluation on word-similarity benchmarks. 

Similarly, other baselines': PCA ```pca_simple.py```, PPA+PCA ```ppa_pca.py``` and PCA+PPA ```pca_ppa.py``` results can be reproduced.

To run the algo and the baselines (as in the paper) get the embedding files ([Glove](https://nlp.stanford.edu/projects/glove/), [FastText](https://github.com/facebookresearch/fastText/blob/master/pretrained-vectors.md)) and put the file locations as required in the code.

The code will generate and evaluate (on 12 word-similarity datasets) a modified word embedding file that is half-the-size of the original embeddings. 

The sentence-vector evalution is based on SentEval (https://github.com/facebookresearch/SentEval). The generated embedding file could be directly used following the SentEval bow.py example.

The algorithm can be used to generate embeddings of any size, not necessarily half.

Another paper which partially uses this code is [On Dimensional Linguistic Properties of the Word Embedding Space](https://arxiv.org/abs/1910.02211).
