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

See this [<font color="blue">PDF file</font>](https://xiaoruiyin.github.io/pdff/BNS013.pdf).

The proof of the following theorem is missing in the beamer. 

**Th(Dedekind)**. $p$ est un entier premier ne divisant pas l'indice of $\mathbb{Z}[\theta]$ ,$\theta$ est integral sur $\mathbb{Q}$ ayant le polynôme minimal $F(X)$, son image canonique dans $\mathbb{Z}/p\mathbb{Z}$ est factorisé dans un produit de polynômes irréductibles $\widetilde{F}=\prod_{k=1}^g\widetilde{F_k}^{e_k}$.
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

**Cor** For any odd prime $p$ and quadratic field $K=\mathbb{Q}(\sqrt{d})$,

$$(\frac{d}{p})=1 \Leftrightarrow (p)=\mathfrak{ab},\ \mathfrak{a,b}\text{ are different prime ideals of }\mathcal{O}_K.$$

$$(\frac{d}{p})=-1 \Leftrightarrow (p) \text{ is a prime ideal of }\mathcal{O}_K.$$

This provides another point of view of the Legendre symbol, we will use it to prove the quadratic reciprocity law.

# Part II, Ramifications(1)

我们用更局部的办法简单看一下差不多的内容,但是这样的办法可以走得更远,顺便也当作熟悉一下处理局部的办法.

$A$ is a Dedekind Domain, $K=\mathrm{Quot}(A)$ its quotient field, field extension $L/K$ finite separable, $B$ the integral closure of $A$ in $L$. $\mathfrak{p}$ is a prime ideal of $A$ and $(\mathfrak{q}
_
i)
_
{1\le i\le g}$ prime ideals of $B$ lying over $\mathfrak{p}$.

$K_\mathfrak{p}$ is the completion of $K$ with regard to $\mathfrak{p}$. $\mathcal{O}_\mathfrak{p}$ its valuation ring.

$e(\mathfrak{p},\mathfrak{q})$ stands for the ramification index of $\mathfrak{p}$ with regard to $\mathfrak{q}$; $f(\mathfrak{p},\mathfrak{q})$ stands for the residual degree.

**Recall.** 1) $B$ is finitely generated over $A$;

 2) $A/\mathfrak{p}^n \simeq \mathcal{O}_
\mathfrak{p}/\mathfrak{p}\mathcal{O}_\mathfrak{p}$;

 3) $\varprojlim_n A/\mathfrak{p}^n \simeq \mathcal{O}_\mathfrak{p}.$

By CRT we have $B/\mathfrak{p}^n B\simeq \prod_{i=1}^g B/\mathfrak{q_i}^{e_in} $. Apply the inverse limit on both side and we get $\varprojlim_n B/\mathfrak{p}^n B\simeq \prod_{i=1}^g \mathcal{O}_\mathfrak{q_i}.$


**Prop1.** $K_\mathfrak{p}\otimes_K L\simeq \prod_{i=1}^g L_\mathfrak{q_i}.$

**Proof.** We show that

$$K_\mathfrak{p}\otimes_K L\to \prod_{i=1}^g L_\mathfrak{q_i},\ x\otimes y\mapsto x\iota(y)$$ where $\iota$ is the diagonal embedding of $L$ in $\prod_{i=1}^g L_\mathfrak{q_i}$ is an isomorphism. 

Clearly it is a monomorphism. To show that it is a surjection, take $(w_i)_{1\le i\le n}$ a integral basis of $B$, it suffices to show that elements of the form $x\iota(w_i)$ generate the whole space.

In applying $\varprojlim_n -/\mathfrak{p}^n -$ on $A^{\oplus n}\xrightarrow{\thicksim} B$ we get an isomorphism $\mathcal{O}_
\mathfrak{p}^{\oplus n}\xrightarrow{\thicksim} \prod_{i=1}^g \mathcal{O}_\mathfrak{q_i}$ and the statement follows. $\square$

**Cor2.** The valuation ring $\mathcal{O}
_
\mathfrak{q}$ of $L
_
\mathfrak{q}$ is the integral closure of $\mathcal{O}
_
\mathfrak{p}.$

**Proof.** It suffices to show that $\mathcal{O}_
\mathfrak{q}$ is finitely generated over $\mathcal{O}
_
\mathfrak{p}$. En effet the isomorphism in the proof of Prop1 embed $\mathcal{O}_
\mathfrak{q}$ into a free $\mathcal{O}_\mathfrak{p}$-Module. $\square$

**Prop3.** Choose $\theta \in B$ s.t. $L=K(\theta)$ and suppose that its minimal polynomial is $F(X)$. The factorisation of $F(X)$ over $K_\mathfrak{p}$ is $F(X)=\prod_{i=1}^h F_i(X).$ Then $h=g$ and 
$K_\mathfrak{p}[T]/(F_i(T))\simeq L_\mathfrak{q_i}$ (except the order of $F_i$).

**Proof.** Let $\tau$ be a $K$-embedding of $L$ in the algebraic closure of $K_\mathfrak{p}/(F)$. Clearly $\tau$ sends a root of $F_i$ to another root of $F_i$. Extend $\tau$ to $L_\mathfrak{q_i}$ then $\tau$ becomes a $K_\mathfrak{p}$-embedding, whose image is contained in exactly one $K_\mathfrak{p}/(F_j)$.

Note that we have the isomorphisms by Prop1 and CRT

$$\prod_{i=1}^g L_\mathfrak{q_i} \to K_\mathfrak{p}[T]/(F) \to \prod_{i=1}^h K_\mathfrak{p}[T]/(F_i)$$

therefore each $L_\mathfrak{q_i}$ is isomorphic to some $K_\mathfrak{p}/(F_j).$ $\square$

**Cor4.** 

 $$[L:K]=\sum_{i=1}^g[L_\mathfrak{q_i}:K_\mathfrak{p}];$$


 $$\mathrm{N}
 _
 {L/K}=\prod_{i=1}^g \mathrm{N}_{L
 _
 \mathfrak{q_i}/K
 _
 \mathfrak{p}};$$


 $$\mathrm{Tr}
 _
 {L/K}=\sum_{i=1}^g \mathrm{Tr}
 _
 {L_\mathfrak{q_i}/K_\mathfrak{p}}.$$


**Cor5.** The following propositions are equivalentes.

1) $\mathfrak{p}$ splits completely in $L$;

2) $F(T)$ splits in $K_\mathfrak{p}$;

3) $K_\mathfrak{p}\simeq L_\mathfrak{q_i}$ for all $i$.

**Prop6.** $e(\mathfrak{p},\mathfrak{q})=e(\mathfrak{p}\mathcal{O}
_
\mathfrak{p},\mathfrak{q}\mathcal{O}
_
\mathfrak{q}),$ $f(\mathfrak{p},\mathfrak{q})=f(\mathfrak{p}\mathcal{O}
_
\mathfrak{p},\mathfrak{q}\mathcal{O}
_
\mathfrak{q}).$

这完全是完备化的性质.

**Prop7.** $$[L:K]=\sum_{i=1}^ge(\mathfrak{p},\mathfrak{q_i})f(\mathfrak{p},\mathfrak{q}).$$

**Proof.** By Cor4.(1) and Prop6. we may suppose $L, K$ are local fields. In this case $\mathcal{O}
_
\mathfrak{p}$ is a PID, $\mathcal{O}
_
\mathfrak{q}$ is a 
$\mathcal{O}
_
\mathfrak{p}$-Module of no torsion, hence free. Suppose that $(\alpha)=\mathfrak{q}.$ Then
$[L:K]=
\mathrm{dim}
_
{\mathcal{O}
_
\mathfrak{p}/\mathfrak{p}\mathcal{O}
_
\mathfrak{p}}\mathcal{O}
_
\mathfrak{q}/\mathfrak{p}\mathcal{O}
_
\mathfrak{q}=\mathrm{dim}
_
{\mathcal{O}
_
\mathfrak{p}/\mathfrak{p}\mathcal{O}
_
\mathfrak{p}}\mathcal{O}
_
\mathfrak{q}/\mathfrak{q}^e=\sum_{i=0}^{e-1}\mathrm{dim}
_
{\mathcal{O}
_
\mathfrak{p}/\mathfrak{p}\mathcal{O}
_
\mathfrak{p}}\alpha^i\mathcal{O}
_
\mathfrak{q}/\alpha^{i+1}/\mathcal{O}
_
\mathfrak{q}=\sum_{i=0}^{e-1}f=ef.$ $\square$


**Lemma.** $$\{
\beta\in L\mid \mathrm{Tr}
_
{L/K}(\beta B)\subset A
\}$$
is a fractional ideal of $B$.

**Proof.** Denote it by $I$. We must prove that it is finitely generated over $A$. Take a $A$-basis $(w_i)$ of $B$ and $(w_i^\vee)$ the dual basis of $(\mathrm{Tr}
_
{L/K}(w_i-))$. Then $\mathrm{Tr}
_
{L/K}(\beta B) \subset A$ iff. $\mathrm{Tr}_{L/K}(\beta w_i) \in A$ for all $i$.

Suppose that $\beta=\sum_i x_iw_i$, $x_i\in K$. Then $\mathrm{Tr}
_
{L/K}(\beta w
_
i^\vee)=\mathrm{Tr}
_
{L/K}(x
_
iw
_
iw
_
i^\vee)nx
_
i\in A$ $\Leftrightarrow$ $\beta \in\sum_i Aw_i.$ 
Hence 
$I\subset \sum_i Aw_i$. $\square$


**Def.** The different of $B$ in $A$ 

$$D(B/A):=\{
\beta\in L\mid \mathrm{Tr}
_
{L/K}(\beta B)\subset A\}^{-1}.$$

**Th8.** Suppose that $K$ is an algebraic number field. Let $\mathfrak{q}$ be a prime ideal of $B$. Then $\mathfrak{q}$ ramifies with regard of $L/K$ iff. $\mathfrak{q}$ divides $D(B/A)$.

We prove this theorem by reduction to local situation.

**Proof.** **Step1** For any $d\in\mathbb{N}$ take $a\in \mathfrak{q}^d\backslash\{0\}$. Consider the commutative diagram

<!-- https://q.uiver.app/#q=WzAsNixbMCwwLCJcXG1hdGhmcmFre3F9XnstZH0vQiJdLFsyLDAsImFeey0xfUIvQiJdLFs0LDAsImFeey0xfUEvQSJdLFsyLDIsIlxccHJvZCDCoGFeey0xfVxcbWF0aGNhbHtPfV9cXG1hdGhmcmFre3AnfS9cXG1hdGhjYWx7T31fXFxtYXRoZnJha3twJ30iXSxbMCwyLCJcXG1hdGhmcmFre3F9XnstZH1cXG1hdGhjYWx7T31fXFxtYXRoZnJha3txfS9cXG1hdGhjYWx7T31fXFxtYXRoZnJha3txfSJdLFs0LDIsIlxccHJvZCDCoGFeey0xfVxcbWF0aGNhbHtPfV9cXG1hdGhmcmFre3AnfS9cXG1hdGhjYWx7T31fXFxtYXRoZnJha3twJ30iXSxbMCwxLCIiLDAseyJzdHlsZSI6eyJ0YWlsIjp7Im5hbWUiOiJob29rIiwic2lkZSI6InRvcCJ9fX1dLFsxLDIsIlxcbWF0aHJte1RyfV97TC9LfSJdLFswLDQsIlxcc2ltIl0sWzIsNSwiXFxzaW0iXSxbMSwzLCJcXHNpbSJdLFs0LDMsIiIsMCx7InN0eWxlIjp7InRhaWwiOnsibmFtZSI6Imhvb2siLCJzaWRlIjoidG9wIn19fV0sWzMsNV1d -->
<iframe class="quiver-embed" src="https://q.uiver.app/#q=WzAsNixbMCwwLCJcXG1hdGhmcmFre3F9XnstZH0vQiJdLFsyLDAsImFeey0xfUIvQiJdLFs0LDAsImFeey0xfUEvQSJdLFsyLDIsIlxccHJvZCDCoGFeey0xfVxcbWF0aGNhbHtPfV9cXG1hdGhmcmFre3AnfS9cXG1hdGhjYWx7T31fXFxtYXRoZnJha3twJ30iXSxbMCwyLCJcXG1hdGhmcmFre3F9XnstZH1cXG1hdGhjYWx7T31fXFxtYXRoZnJha3txfS9cXG1hdGhjYWx7T31fXFxtYXRoZnJha3txfSJdLFs0LDIsIlxccHJvZCDCoGFeey0xfVxcbWF0aGNhbHtPfV9cXG1hdGhmcmFre3AnfS9cXG1hdGhjYWx7T31fXFxtYXRoZnJha3twJ30iXSxbMCwxLCIiLDAseyJzdHlsZSI6eyJ0YWlsIjp7Im5hbWUiOiJob29rIiwic2lkZSI6InRvcCJ9fX1dLFsxLDIsIlxcbWF0aHJte1RyfV97TC9LfSJdLFswLDQsIlxcc2ltIl0sWzIsNSwiXFxzaW0iXSxbMSwzLCJcXHNpbSJdLFs0LDMsIiIsMCx7InN0eWxlIjp7InRhaWwiOnsibmFtZSI6Imhvb2siLCJzaWRlIjoidG9wIn19fV0sWzMsNV1d&embed" width="200" height="200" style="border-radius: 8px; border: none;"></iframe>

> 这个画交换图巨好用,大家都来用.

The products run over all (finitely many) prime ideals containg $a$. The isomorphisms is given by CRT.

Therefore $\mathfrak{q}^{d}$ divides $D(B/A)$ iff. the first row sends $\mathfrak{q}^{-d}B/B$ to 0 iff. the second row sends $\mathfrak{q}^{-d}\mathcal{O}
_
\mathfrak{q}/\mathcal{O}
_
\mathfrak{q}$ to 0 iff. $\mathfrak{q}^{d}\mathcal{O}
_
\mathfrak{q}$ divides 
$D(\mathcal{O}
_
\mathfrak{q}/\mathcal{O}_
\mathfrak{p}).$

**Step2**. Now we may assume that $L,K$ are local. Note that $\mathfrak{q}/\mathfrak{p}B$ is torsion, 
$\mathrm{Tr}
_
{L/K}(\mathfrak{q}/\mathfrak{p}B)=\mathrm{tr}(\text{nilpotent matrix})=0.$ 
That is to say $\mathrm{Tr}
_
{L/K}(\mathfrak{q})\subset \mathfrak{p}$ and $\mathrm{Tr}
_
{L/K}(\mathfrak{p}^{-1}\mathfrak{q})\subset A,$ i.e. $\mathrm{Tr}
_
{L/K}(\mathfrak{q}^{1-e})\subset A$. 

Therefore $\mathfrak{q}^{1-e}\subset D(B/A)^{-1}$, so $\mathfrak{q}^{e-1}$ divides $D(B/A)$.

So $\mathfrak{q}$ is ramified i.e. $e\geq 2$ implies $\mathfrak{q}$ devides $D(B/A)$.

Conversely suppose that $e=1$, then $B/\mathfrak{p}B$ is a field, and is a finite extension of $A/\mathfrak{p}$. Then $\mathfrak{q}$ divides $D(B/A)$ implies $\mathrm{Tr}
_
{L/K}(\mathfrak{q}^{-1})=\mathrm{Tr}
_
{L/K}(\mathfrak{p}^{-1}B)\subset A$, so $\mathrm{Tr}
_
{L/K}(B)\subset \mathfrak{p}A$. Hence $\mathrm{Tr}
_
{L/K}(B/\mathfrak{p}B)=0$ and it follows that the extension $B/\mathfrak{p}B\mid A/\mathfrak{p}$ is not separable, a contradiction. $\square$

关于上面的step1首先是我觉得有 $A/I\simeq I^{-1}/A$ .另外关于后面两列的同构原书上写的是过遍全部素理想,然后一开始我没有意识到这其实是个有限乘积于是没想明白,就跑去问了同学和老师.善良的老师还告诉我老百姓我们可以考虑一个更加奢侈的版本 $\mathbb{Q}\otimes_\mathbb{Z}\hat{\mathbb{Z}}/\hat{\mathbb{Z}}\simeq \mathbb{Q}/\mathbb{Z}$ (看起来是汇集了所有素数信息的一个无穷的东西,但实际上这个同构也差不多是CRT给的).

**Prop9.** $L=K(\theta)$, $\theta$ integral, $F$ its minimal polynomial. Then $$\{\beta\in L\mid \mathrm{Tr}_{L/K}(\beta A[\theta])\subset A\}=\frac{1}{F'(\theta)}A[\theta].$$

**Proof.** $\frac{1}{F'(\theta)}A[\theta]$ has $A$-basis $(\frac{\theta^i}{F'(\theta)})$, so it suffices to show that
$$(\mathrm{Tr}
_
{L/K}(\frac{\theta^{i+j}}{F'(\theta)}))_{0\le i,j\le n-1}\in \mathrm{GL}_n(A).$$

We consider $(\alpha_i)$ the roots of $F$ in the algebraic closure of $K$. We have

$$\mathrm{Tr}
_
{
L/K}(\frac{\theta^{m}}{F'(\theta)})=\sum\frac{\alpha_i^{m}}{F'(\alpha_i)}=\sum\frac{\alpha_i^{m}}{\prod_{j\neq i}(\alpha_j-\alpha_i)}.$$

Therefore $\mathrm{Tr}
_
{L/K}(\frac{\theta^{m}}{F'(\theta)})$ is $x^{n-1}$ coefficient of $x^m=\sum\alpha_i^{m}\prod_{j\neq i}\frac{(x-\alpha_i)}{(\alpha_j-\alpha_i)}.$ $\square$

**Cor10.** Suppose that $B=A[\theta]$, then $D(B/A)=(F'(\theta)).$

**Def.** Unramified extension: $e=1$, $f=n$, residue field separable.

注意我们这里都是离散赋值所以第一条保证第二条.对于成立FNP的环比如各种代数整数环最后一条则自动成立.

**Prop11.** Suppose that $K$ is a complete discrete valuation field and $F$ its residue field. We have the bijection correspondance (except an isomorphism) between
$$\{\text{unramified extensions of }K\}\leftrightarrow\{\text{finite separable extensions of }F\}$$
satisfying

1) It preserves the degrees of extensions;

2) It preserves Galois extensions and their Galois group.

The correspondance is given by

For $E/F$ finite separable suppose that $E=F(\beta)$ and denote the minimal polynomial of $\beta$ by $f(T)\in F[T]$. Lift it into $A[T]$ then $f$ is still irreducible. We maps $E$ to $L=K(\alpha)$ where $\alpha$ is a root of $f$ in the algebraic closure of $K$.

**Proof.** i) This map is well-defined. By Cor10 $D(B/A)=(f'(\beta))\neq 0$ with regard to $E/F$,therefore $\mathfrak{p}$ does not divide $D(B/A)$,hence $L$ is unramified. 

ii) For any unramified extension $L$ of $K$ we maps $L$ to its residue field $E$. We show that this defines the inverse of the given map. We write the factorisation of $f$ in $L$ $f=\prod f
_
i.$
Note that all roots of $f
_
i$ are integral over $A$, it follows that
f
_
i[T]\in B[T].
WLOG $f
_
1(\beta)=0$ in $E$.
Lift $f
_
1$ to $K[T]$ and we add a root $\alpha$ of $f
_
1$ to $L$. $f
_
1'(\alpha)\neq 0$ in E $\Rightarrow$ $L(\alpha)/L$ unramified.

The residue field of $L(\alpha)$ is $E[T]/(f
_
1)=E$, so $e(L(\alpha)/K)=e(L/K)$, $f(L(\alpha)/K)=f(L/K)$. Therefore $[L(\alpha):L]=[L(\alpha):K]/[L:K]=1$ i.e. $L=L(\alpha).$ Particularly $K(\alpha)\subset L.$ Again we have $[K(\alpha):K]\geq [F(\beta):F]=[E:F]=[L:K]$, so $K(\alpha)=L$.

iii) $[E:F]=\mathrm{deg}(f)=[L:K].$

iv) When $L=K(\alpha)$ is a Galois extension we have $L=K[T]/(f).$ and $E=F[T]/(f)$ so $E/F$ is Galois. Therefore 
$\mathrm{Card}(\mathrm{Gal}(L/K))=\mathrm{Card}(
\mathrm{Gal}(E/F))$. Viewing them as a subgroup of the permutation group of the roots of $f$ in $L$ and $E$, we get a natural monomorphism 
$\mathrm{Gal}(L/K)\to \mathrm{Gal}(E/F).$ By the finiteness this is a bijection. $\square$

最后我们看一下Galois的情况就结束,剩下的有机会再写.

In the following part we may assume that $L/K$ is a finite Galois extension.

**Def.** Decomposition group of $\mathfrak{q}$
$$D
_
\mathfrak{q}=
\
{
\sigma\in\mathrm{Gal}(L/K)\mid\sigma\mathfrak{q}=\mathfrak{q}
\
}
.
$$

**Prop12.** $L_\mathfrak{q}/K_\mathfrak{p}$ Galois. Isomorphism $\mathrm{Gal}(L_\mathfrak{q}/K_\mathfrak{p})\to D
_
\mathfrak{q}, \sigma\mapsto\sigma\mid
_
L.$

**Prop13.** $\mathrm{Gal}(L/K)$ acts transitively on prime ideals of $B$ lying over $\mathfrak{p}$.

**Proof.** Denote $X$ the set of prime ideals of $B$ lying over $\mathfrak{p}$. We must show that for all $\mathfrak{q}$ we have $\mathrm{Gal}(L/K)\mathfrak{q}=X.$ Clearly $\mathrm{Gal}(L/K)\mathfrak{q}\subset X.$
We have $$[L:K] = \sum
_
{\mathfrak{q}\in X}[L
_
\mathfrak{q}:K
_
\mathfrak{p}]$$
and
$$[L:K]=\mathrm{Gal}(L/K)=\mathrm{Card}(\mathrm{Gal}(L/K)\mathfrak{q})\mathrm{Card}(D
_
\mathfrak{q})=\mathrm{Card}(\mathrm{Gal}(L/K)\mathfrak{q})[L
_
\mathfrak{q}:K
_
\mathfrak{p}]=
\sum
_
{\mathfrak{q}\in\mathrm{Gal}(L/K)\mathfrak{q} }[L
_
\mathfrak{q}:K
_
\mathfrak{p}]$$

Hence $\mathrm{Card}(\mathrm{Gal}(L/K)\mathfrak{q})=\mathrm{Card}( X).$ $\square$

顺便这里面很多术语很难不让人想到Riemann surfaces,也许我们以后可以看到它在那里的类似物.

这部分证明有几个是我自己写的,因为我老百姓愚笨,书上的我没理解或者我觉得他没说清楚,如果发现我写错了敬请指正.

这个note断断续续施工一周左右,基本上是我拿记事本写,写一段差不多了就复制出来预览一下然后改改小错误,我觉得书写体验不差于overleaf,远好于BNS的微信公众号(虽然这个也是拿记事本写).写的过程中也意外地发现一些我第一遍抄书时候理解错或者自己证明证错的地方.感觉虽然没有人和我组讨论班但是可以作为“尝试解释清楚一个东西”的替代物,就是效率要低很多.

至于这节最重要的结论(沿用上个pdf里面的记号)我觉得是 $p\mid d_K$ $\Leftrightarrow$ $p$ $ramifies$,它是Th8和Cor10的推论. 纯初等手法可以证到必要性,但是好长啊就没有打进上面的beamer.

虽然L3上的课好简单但是好累人啊,不过也是因为到了不得不思考顶着浑身debuff如何升学的时候.本来建设这个就是想要既放松一下又能复习一下数学的,结果还是很累,就这样,歇了,下次有什么再写.
