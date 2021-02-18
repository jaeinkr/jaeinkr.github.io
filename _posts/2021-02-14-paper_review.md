---
layout: default
title : "Complex Embeddings for Simple Link Prediction (2016)" 
categories: [Paper Notes]
tags: [NLP, Research, Link Prediction]
use_math: true
---
<p>{{ page.date || date_to_long_string }} </p>
## [Paper Note] [Complex Embeddings for Simple Link Prediction](http://proceedings.mlr.press/v48/trouillon16.pdf) (2016)
#### Theo Trouillon, Johannes Welbl, Sebastian Riedel, Eric Gaussier, Guillaume Bouchard
>Keywords: NLP, Link Prediction, Embedding Model, Complex Embedding 

<br>
### Task Statements

Natural redundancies among the recorded relations often make it possible to ﬁll in the missing entries of a KB. As an example, the relation CountryOfBirth is not recorded for all entities, but it can easily be inferred if the relation CityOfBirth is known. The goal of link prediction is the automatic discovery of such regularities.i
However, many relations are non-deterministic: the combination of the two facts IsBornIn(John,Athens) and IsLocatedIn(Athens,Greece) does not always imply the fact HasNationality(John,Greece).



Finding the best ratio between expressiveness and parameter space size is the keystone of embedding models. -> trade-off

<br>
### Motivation

the link prediction problem is key to automatically understand the structure of large knowledge bases. 
solve this problem through latent factorization


<br>
### Background
popular method is to state the link prediction task as a 3D binary tensor completion problem, where each slice is the adjacency matrix of one relation type in the knowledge graph.

Completion based on low-rank factorization or embeddings has been popularized with the Netﬂix challenge (Koren et al., 2009). 
A partially observed matrix or tensor is decomposed into a product of embedding matrices with much smaller rank, resulting in ﬁxed-dimensional vector representations for each entity and relation in the database. 
For a given fact r(s,o) in which subject s is linked to object o through relation r, the score can then be recovered as a multi-linear product between the embedding vectors of s, r and o

<br>
### Contributions

<br>
### Notation and background


<br>
### Method
However, here we make use of complex valued embeddings.
The composition of complex embeddings can handle a large variety of binary relations, among them symmetric and antisymmetric relations.


<br>
### Conclusions
Compared to state-of-the-art models such as Neural Tensor Network and Holographic Embeddings, our approach based on complex embeddings is arguably simpler

Our approach is scalable to large datasets as it remains linear in both space and time, while consistently outperforming alternative approaches on standard link prediction benchmarks.
