NLP Paper Reading Notes
===

***1. A Simple But Hard-to-Beat Baseline for Sentence Embedding***

Address: https://openreview.net/forum?id=SyK00v5xx

This paper proposed a simple sentence embedding method —— Smooth Inverse Frequency (SIF).
Given word embeddings,
First, sum all word embedding in a sentence with weight as follow：
$$v_{s}$$
Then, form a matrix which columns consist of sentence embedding from above operation and let u be its first singular vector
