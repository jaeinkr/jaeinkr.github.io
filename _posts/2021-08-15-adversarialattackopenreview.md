---
layout: post
title : "Survey of Adversarial Attacks from Accept/Reject Perspectives (1/2)" 
categories: [Paper Notes]
use_math: true
---


> [OpenReview.net](https://openreview.net/)에서 리뷰어들의 코멘트와 저자의 답변, 그리고 Accept/Reject 여부를 바탕으로 정리한 Adversarial Attacks 서베이입니다.

_All image credits of this post: the original papers._

## Papers to explore
---
This survey cover the following papers including both accepted and rejected papers:
- [Towards Robustness Against Natural Language Word Substitutions](
https://openreview.net/forum?id=ks5nebunVn_)
- [Generating universal language adversarial examples by understanding and enhancing the transferability across neural models](https://openreview.net/forum?id=_QQ_v_w_uNV&noteId=Mr5Cgg-rsA-)
- [Neural Attention Distillation: Erasing Backdoor Triggers from Deep Neural Networks](https://openreview.net/forum?id=9l0K4OM-oXE)
- [Robust anomaly detection and backdoor attack detection via differential privacy](https://openreview.net/forum?id=SJx0q1rtvS)
- [Poisoned classifiers are not only backdoored, they are fundamentally broken](https://openreview.net/forum?id=zsKWh2pRSBK)
- [Clean-Label Backdoor Attacks](https://openreview.net/forum?id=HJg6e2CcK7)
- [Universal Attacks on Equivariant Networks](https://openreview.net/forum?id=B1MX5j0cFX&noteId=ryg8nMgR3Q)
- [Dynamic Backdoor Attacks Against Deep Neural Networks](https://openreview.net/forum?id=6s480DdlRQQ)
- [Greedy Attack and Gumbel Attack: Generating Adversarial Examples for Discrete Data](https://openreview.net/forum?id=ByghKiC5YX&noteId=Syg18fj11E)
- [Just How Toxic is Data Poisoning? A Benchmark for Backdoor and Data Poisoning Attacks](https://openreview.net/forum?id=c77KhoLYSwF)
- [Fooling a Complete Neural Network Verifier](https://openreview.net/forum?id=4IwieFS44l)
- [Unrestricted Adversarial Attacks For Semantic Segmentation](https://openreview.net/forum?id=rkx6MJSFPH)
-[Black-Box Adversarial Attack with Transferable Model-based Embedding](https://openreview.net/forum?id=SJxhNTNYwB)
- [BREAKING CERTIFIED DEFENSES: SEMANTIC ADVERSARIAL EXAMPLES WITH SPOOFED ROBUSTNESS CERTIFICATES](https://openreview.net/forum?id=HJxdTxHYvB)
- [SemanticAdv: Generating Adversarial Examples via Attribute-Conditional Image Editing](https://openreview.net/forum?id=r1l-VeSKwS)
- [Pragmatic Evaluation of Adversarial Examples in Natural Language](https://openreview.net/forum?id=BkxmKgHtwH)
- [BadNL: Backdoor Attacks Against NLP Models](https://openreview.net/forum?id=v6UimxiiR78&noteId=pn3JiXG1cz)

_Part of the papers are surveyed in this post. The next post will cover the remains._
<br>
_(More papers may be added)_

<br>
## 1. Towards Robustness Against Natural Language Word Substitutions
---
_ICLR 2021 Spotlight_
<br>
_Xinshuai Dong, Anh Tuan Luu, Rongrong Ji, Hong Liu_
<br>

**The Idea:**
The proposed method ASCC(Adversarial Sparse Convex Combination) captures adversarial word substitutions in the vector space using a convex hull towards robustness. Using a convex hull can satisfy three aspects: inclusiveness, exclusiveness, and optimization. 
<center><img src="/assets/img/210815-1.png" width="90%" height="90%"></center>

<center><img src="/assets/img/210815-2.png" width="90%" height="90%"></center>

**One-sentence Summary of the Reviews**:
The idea is straightforward, experiments are well designed and quantitative.

<br>
## 2. Generating universal language adversarial examples by understanding and enhancing the transferability across neural models
---
_ICLR 2021 Conference Withdrawn Submission_
<br>
_Liping Yuan
, Xiaoqing Zheng
, Yi Zhou, Cho-Jui Hsieh, Kai-Wei Chang, Xuanjing Huang_

**The Idea**:
This paper studies the adversarial transferability across different models on NLP, varying different properties such as model architecture and size. Extensive experiments have been conducted to evaluate which factors can affect the transferability most.

**One-sentence Summary of the Reviews**:
There are some doubtful experimental settings and the conclusion of this paper is not clear.

<br>
## 3. Neural Attention Distillation: Erasing Backdoor Triggers from Deep Neural Networks
---
_ICLR 2021 Poster_
<br>
_Yige Li, Xixiang Lyu, Nodens Koren, Lingjuan Lyu, Bo Li, Xingjun Ma_

**The Idea**:
This paper presents an empirical study on the backdoor erasing in CNN via teacher-student alignment of the attention maps, which treats the poisoned model as the student and the fine-tuned model as the teacher. 

<center><img src="/assets/img/210815-3.png" width="90%" height="90%"></center>
<br>
**One-sentence Summary of the Reviews**:
Well-written paper including sufficient experiment, but the behavior of NAD is not completely understood.

<br>
## 4. Robust anomaly detection and backdoor attack detection via differential privacy
---
_ICLR 2020 Poster_
<br>
_Min Du, Ruoxi Jia, Dawn Song_

**The Idea**:
This paper leverages differential privacy’s (DP) stability properties to investigate its use for improved outlier and novelty detection. Under the assumption that a well-trained model would assign a higher loss on the outliers, the paper gives a theoretic bound on how this loss will decrease if there are poisoned samples in the training set. 

**One-sentence Summary of the Reviews**:
The paper is well-written but contributions are not substantial.

<br>
## 5. Poisoned classifiers are not only backdoored, they are fundamentally broken
---
_ICLR 2021 Conference Withdrawn Submission_
<br>
_Mingjie Sun, Siddhant Agarwal, J Zico Kolter_

**The Idea**:
The authors showed that with some post-processing analysis on a poisoned classifier, it is possible to construct effective alternative triggers against a backdoor classifier. Specifically, adversarial samples that are generated against models robustified with Denoised Smoothing often show backdoor patterns.  

**One-sentence Summary of the Reviews**:
The presented approach is mainly manual and needs human inspection.



<br>
<br>
_Next Post: [Survey of Adversarial Attacks from Accept/Reject Perspectives (2/2)]() (soon be updated)_
