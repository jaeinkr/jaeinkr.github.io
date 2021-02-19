---
layout: post
title : "Complex Embeddings for Simple Link Prediction (2016) (1)"
categories: [Paper Notes]
tags: [NLP, Research, Link Prediction]
use_math: true
published: false
---
#### Theo Trouillon, Johannes Welbl, Sebastian Riedel, Eric Gaussier, Guillaume Bouchard
>Keywords: NLP, Link Prediction, Embedding Model, Complex Embedding

[paper link](https://arxiv.org/pdf/1606.06357.pdf)

_Statement: I recently started posting paper reviews in my blog for my research on NLP. 
However, I am not yet a professional researcher as well as English is not my native language so that my posts might have some incorrect descriptions.
I hope whoever reading my post understand my situation and I will be very grateful if you correct any wrong information. <3
The comment section will be added to my blog very soon!!_

_In this post, I only describe general concepts of this paper. Detailed theoretical contents will be introduced in the next post._

## Motivation and General Idea
---

In link prediction, many relations are non-deterministic. 
For example, the combination of the two facts _IsBornIn(John, Athens)_ and _IsLocatedIn(Athens, Greece)_ 
does not always imply _HasNationality(John, Greece)_ is true.

To do so, the authors believe it is required to handle them in a probabilistic fashion involving the properties sucn as reflexivity, symmetry and transitivity.
In the previous works, dealing with _anti-symmetric_ relations always implied an explosion of the number of parameters making models prone to overfitting.
So that the finding the best ratio between expressiveness and parameter space size is the keystone of embedding models while dealing with anti-symmetric relations:
<center><img src="/assets/img/210218_1.png" width="80%" height="80%"></center>

To address this, in this work, *complex embeddings* are used instead of real-number embeddings, which involves **_Hermitian_** dot prodoct. 
In this way, it is able to take advantages of both of:
- dot product -> linearity in both space and time complexity
- complex vectors -> capture antisymmetric relations

<br>

## Contributions
---

The author applied complex values to latent factorization calculations to induce efficient handling of antisymmetric relations.
Compared with the existing SOTA models, this approach is more "simple" since it uses only the Hermitian dot product.
Also, since it is linear in space and time, it can be applied to large datasets.

At last, The author gave some suggestions on possible future works. 
The first is merging their approaches to known tensor factorization in order to improve predictive performance. For example, parewise embeddings and complex numbers being used together 
might lead to the works involve non-compositionality.
Another one is to develop negative sampling procedure to generate informative nagative samples.

