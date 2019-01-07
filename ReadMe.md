NLP Paper Reading Notes
===

***1. A Simple But Hard-to-Beat Baseline for Sentence Embedding***

Address: https://openreview.net/forum?id=SyK00v5xx

This paper proposed a simple sentence embedding method —— Smooth Inverse Frequency (SIF).
Given word embeddings,
First, sum all word embedding in a sentence with weight as follow：

<a href="https://www.codecogs.com/eqnedit.php?latex=v_{s}&space;=&space;\frac{1}{|s|}&space;\sum_{w\in&space;sentence}&space;\frac{a}{a&plus;freq(w)}&space;v_{w}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?v_{s}&space;=&space;\frac{1}{|s|}&space;\sum_{w\in&space;sentence}&space;\frac{a}{a&plus;freq(w)}&space;v_{w}" title="v_{s} = \frac{1}{|s|} \sum_{w\in sentence} \frac{a}{a+freq(w)} v_{w}" /></a>
where, a is a connstant.(0.001 or 0.0001 could lead to best results)

Then, form a matrix which columns consist of sentence embedding from above operation (eg.[v1.T, v2.T,...,vn.T]) and let u be its first singular vector. 

Finally:<a href="https://www.codecogs.com/eqnedit.php?latex=v_{s}&space;=&space;v_{s}&space;-&space;uu^{T}v_{s}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?v_{s}&space;=&space;v_{s}&space;-&space;uu^{T}v_{s}" title="v_{s} = v_{s} - uu^{T}v_{s}" /></a>
