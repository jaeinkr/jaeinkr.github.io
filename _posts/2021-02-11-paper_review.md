---
layout: default
title : "[Paper Note] SimplE Embedding for Link Prediction in Knowledge Graphs (2018)" 
categories: [Paper Notes]
tags: [NLP, Research, Link Prediction]
use_math: true
---
<p>{{ page.date || date_to_long_string }} </p>
## [Paper Note] [SimplE Embedding for Link Prediction in Knowledge Graphs](https://arxiv.org/pdf/1802.04868.pdf) (2018)
#### Authors: Seyed Mehran Kazemi, David Poole
>Keywords: NLP, Link Prediction, Embedding

<br>
### Task Statements
_**Link Prediction**_ is a task of Knowledge Graph (KG), and its definition is as follows. 
KG is composed of many triples, where each triple is represented by _(head, relation, tail)_, and the goal of Link Prediction is to predict new triples using given triples to make a complete KG. 
This paper proposed an embedding model **SimplE** based on the Canonical Polyadic (CP) decomposition method which is one of tensor factorization methods. 
According to the authors, while SimplE overperforms many existing SOTA models based on tensor factorization approach, it is 'simpler', interpretable and expressive. 

<br>
### Motivation
_Canonical Polyadic (CP) decomposition is among the first tensor factorization approaches. CP generally performs poorly for link prediction as it learns two independent embedding vectors for each entity, whereas they are really tied._

<br>
### Contributions
- Presented a simple enhancement model of CP, **SimplE**, to allow the two embeddings of related each entity to be learned dependently.
- Used the **inverse of relations** to address the **independence of the entity vectors** in CP. 
(In experient, comparing _SimplE_ and _SimplE-ignr_ demostrates the effectiveness)

<br>
### Notation and background
- $E$ and $R$ represent the set of entities and relations; 
- $(h, r, t)$ represents a triple, where $h ∈ E$, $r ∈ R$, $t ∈ E$;
- $ζ$ represent the set of all true triples and $ζ′$ represents all false triples, so that a $KG$ is a subset of $ζ$.
- Whereas the previous embedding models of Link Prediction tended to learn by equating head embedding and tail embedding, SimplE separates the head and tail and trains them independently. In the process, embedding is learned more efficiently by using Symmetry, anti-symmetry, and inversion.
- Tensor decomposition is a concept that is widely used in recommendation and prediction models. It works by decomposing a sparse matrix and filling the original matrix for prediction. CP decomposition is also one of these decomposition methods.


<br>
### Method
#### *SimplE* is fully exppressive

> Proposition 1. 
For any ground truth over entities $E$ and relations $R$ containing $γ$ true facts, there exists a SimplE model with embedding vectors of size $min(|E| · |R|, γ + 1)$ that represents that ground truth.

The paper gives other examples of the expressiveness of other existing models that might help for understanding:
 "*DistMult* is not fully expressive as it forces relations to be symmetric. It has been shown in that *ComplEx* is fully expressive with embeddings of length at most $|E|{\cdot}|R|$." 


#### Incorporating background knowledge into the embeddings
In _SimplE_, each element of the embedding vector is considered as a feature, and each one represents how important that feature is to the relation.

The implemented properties are:
- Symmetric
- Anti-symmetric
- Inverse
- Reflexive

The advantages of incorporating operations are:
- It allows the embeddings to be potentially transferred to other domains.
- It allows for incorporating observed features into the embeddings.
- It helps reduce the size of the embedding.


 The reason why the paper could achieve fast computation speed by two to four times over the contrasting model _ComplEx_ is that, it removed redundant elements in various ways, including the techniques mentioned above.

<br>
### Conclusions
The experimental results shows the performance of SimplE is comparable to or superior to the existing models, while faster and more efficient learning is possible.\
Nowadays, language models such as GPT-2 and GPT-3, which are trained with billion-parameter or even trillion-parameter that requires enormous computation resources, are in the spotlight in NLP research. 
However, that also led many AI research to focus on conducting lightweight and efficient models capable of fast learning with a small amount of resources.
