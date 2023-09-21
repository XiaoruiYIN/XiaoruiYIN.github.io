---
date: 2023-09-20
layout: post
title: BNSnote013 Factorization in Dedekind Domains & Ramifications
subtitle: 
description: 
image: https://raw.githubusercontent.com/XiaoruiYIN/gtiobnsimg/main/img/IMG_0660.jpg
optimized_image: https://raw.githubusercontent.com/XiaoruiYIN/gtiobnsimg/main/img/IMG_0660.jpg
category: Mathematics
tags:
  - BNS
  - Mathematics
author: X.YIN
math: true
---

> References : 	加藤　和也, 黒川　信重, 斎藤　毅, 数論I Fermatの夢と類体論; Sudesh Kaur Khanduja, A Textbook of Algebraic Number Theory.

# Part I, Dedekind Domain

In this part we establish some properties of Dedekind domains and $\mathcal{O}_K$ and some basic results of ramifications.

[<font color="blue">PDF file</font>](https://xiaoruiyin.github.io/pdff/BNS013.pdf) of part I.

The proof of the following theorem here is missing in the beamer. 

**Theorème(Dedekind)**. $p$ est un entier premier ne divisant pas l'indice of $\mathbb{Z}[\theta]$ ,$\theta$ est integral sur $\mathbb{Q}$ ayant le polynôme minimal $F(X)$, son image canonique dans $\mathbb{Z}/p\mathbb{Z}$ est factorisé dans un produit de polynômes irréductibles $\widetilde{F}=\prod_{k=1}^g\widetilde{F_k}^{e_k}$.
    Alors la factorisation de l'idéal $(p)$ est $(p)=\prod_{k=1}^g(p,F_k(\theta))^{e_k}$.

**Proof(sketch)**. Dénote $\mathfrak{p}_k=(p,F_k(\theta))$. 

_Step1_  Mq $\mathfrak{p}_k$ est un idéal propre, donc $\mathfrak{p}_k$ est maximal.
> sinon $(p)$ et $(F_k(\theta))$ sont premiers entre eux.

_Step2_  $\mathfrak{p}_i=\mathfrak{p}_j$ iff. $i=j$. 
> sinon comme $F_iU+F_jV=1+pW$ où $U, V, W$ dans $\mathbb{Q}[X]$, on aura $1\in\mathfrak{p}_i$.

_Step3_  Mq $(p)=\prod_{k=1}^h\mathfrak{p}_k^{l_k}$ où $l_k\leq e_k$.
> supposons que ${A_k\mathfrak{p}_k=(F_k(\theta))}$ $\text{et}$ $B_k\mathfrak{p}_k=(p)$.

> $A_k,B_k$ sont premiers entre eux. Note que $B_k\mid(p)\mid(\prod_{k=1}^gF_k^{e_k}(\theta))=\prod_{k=1}^g\mathfrak{p}_k^{e_k}A_k^{e_k}$. 

> En déduire que $(p)\mid \prod_{k=1}^g\mathfrak{p}_k^{e_k}$.

_Step4_  Mq $e_k=l_k$. 
> on a déjà $\sum_{k=1}^ge_k\mathrm{deg}F_k=n$. $\prod_{k=1}^gF_k^{l_k}(\theta)\in (p)$ $\Rightarrow$ $\sum_{k=1}^gl_k\mathrm{deg}F_k\geq \mathrm{dim}_{\mathbb{Z}/p\mathbb{Z}}\mathcal{O}_K/p\mathcal{O}_K=n$.

_Step5_  Mq $f_k=\mathrm{deg}F_k$.
> Notons que l'extension des corps $\mathbb{Z}/p\mathbb{Z}\hookrightarrow\mathcal{O}_K/\mathfrak{p}_k$ est normale (ces deux corps sont finis) et que $\theta+\mathfrak{p}_k$ annule $\widetilde{F_k}$, donc $\widetilde{F_k}$ est scindé dans $\mathcal{O}_K/\mathfrak{p}_k$, alors $f_k=[\mathcal{O}_K/\mathfrak{p}_k:\mathbb{Z}/p\mathbb{Z}]\geq\mathrm{deg}F_k$.

$\square$

Put $K=\mathbb{Q}(\sqrt{d})$ where $d$ is square-free. It follows immediately from the theorem that
**Corollary** For any odd prime $p$ and quadratic field $K=\mathbb{Q}(\sqrt{d})$,

$$\left\(\frac{d}{p}\right\)=1 \Leftrightarrow (p)=\mathfrak{ab},\ \mathfrak{a,b}\text{ are different prime ideals of }\mathcal{O}_K.$$

$$\left\(\frac{d}{p}\right\)=-1 \Leftrightarrow (p)text{ is a prime ideal of }\mathcal{O}_K.$$

This provides another point of view of the Legendre symbol, we will use it to prove the quadratic reciprocity law.

# Part II, Ramifications
