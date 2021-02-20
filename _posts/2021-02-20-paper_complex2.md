---
layout: post
title : "Complex Embeddings for Simple Link Prediction (2016) (2)"
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

_This post is about the theoretical stuff involved in the paper. 
If you want to learn about general idea, please read [this](http://jaeinkr.github.io/paper%20notes/2021/02/18/paper_complex1.html)._


## Intuition of using complex embeddings
---
The author applied complex embeddings on a simplified link prediction task wih a single relation type to introduce the intuition of using it.

Gives examples of normal decompositions with real numbers to discuss why complex embeddings are needed.

$Y_{so}\in \{-1, 1\}$ \\
$P(Y_{so}=1)=sigma(X_{so})$

The goal is to find $X$.

Standard matrix factorization approximates $X$ by a matrix product $UV^T$ where $U$, $V$$\in{\mathbb{R}^{n\times K}}$.\
$\Longrightarrow$ An entity has different embeddings when it appears as a subject or object.

