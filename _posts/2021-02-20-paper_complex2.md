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
So what I wanted to understand is why the complex embeddings are needed. The author applied complex embeddings on a simplified link prediction task with a single relation type to introduce the intuition of using it.

There are some definitions:
- $\varepsilon$ is a set of entities with \|${\varepsilon}$\|=$n$. 
- A relation between two entities is binary value $Y_{so}\in \{-1, 1\}$, where $s, o\in{\varepsilon}$. 
- $s, o$ represents subject and object respectively.

Here, the goal is to find a latent matrix $X\in{\mathbb{R}}^{n\times n}$.
There are many existing matrix factorization approaches, such as _SVD_, to approximate $X$.
However, we have to note that the same entity can appear as both subject and object. 
Naturally, joint embeddings of the entities are learnt in most of link prediction research.
For example, Eigenvalue decomposition is often used to approximate real symmetric matrices such as similarity matrices:

$X = EWE^{-1}$.

But how to make it possible to also be antisymmetric? It is not possible in the real space!
So this is why the complex embeddings are needed in this research.
With complex numbers, the dot product is defined as:

$<u,v>:=\bar{u}^T{v}$,

where $u$ and $v$ are complex vectores. Specifically, $u=Re(u)+iIm(u)$ with $Re(u)\in{\mathbb{R}^K}$ and $Im(u)\in{\mathbb{R}^K}$.
We re-define the matrix $X$ as:

$X=EW\bar{E}^T$.

where $W, E\in{\mathbb{C}^{n\times n}}$ and $E\in{\mathbb{C}^{n\times n}}$.

<!--
Standard matrix factorization approximates $X$ by a matrix product $UV^T$ where $U$, $V$$\in{\mathbb{R}^{n\times K}}$.\
$\Longrightarrow$ An entity has different embeddings when it appears as a subject or object.
-->
