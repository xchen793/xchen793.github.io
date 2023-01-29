---
layout: post
title: TDA Notes(1)
date: 2023-01-28 11:59:00-0400
description: Pipeline, Metric Spaces, Covers, and Simplicial Complexes
categories: learning-notes data-analysis
giscus_comments: false
---

## 1. TDA Pipeline
    1. The input is assumed to be a finite set of points with a notion of distance - or similarity - between them. The distance can be 1) induced by the metric in the ambient space(e.g. 2D? 3D?) or 2) an intrinsic metric defined by a pairwise distance matrix.
    2. 

## 2. Metric Space

$$\textbf{Def 2.1}$$: A metric space ($$M$$, $$\rho$$) is a set $$M$$ with a function $$\rho : M \times M \rightarrow \mathcal{R}_{+}$$, such that $$ \forall x, y, z \in M$$, the following is the case:

i) (Positivity) $$ \rho(x,y) \geq 0$$ and $$\rho(x,y) = 0$$ iff $$x = y$$.

ii) (Symmetry) $$\rho(x,y) = \rho(y,x)$$

iii) (The Triange Inequality) $$\rho(x,z) \leq \rho(x,y) + \rho(y,z)$$

$$\textbf{Def 2.2}$$: A subset $$S \subseteq R$$ is called compact if every sequence in $$S$$ has a subsequence that converges to a point in $$S$$.

$$\textbf{Def 2.3}$$: Given two compact subsets $$A, B \subseteq M$$, the Hausdroff distance $$d_{H}(A,B)$$ between set $$A$$ and set $$B$$ is the smallest nonnegative number $$\delta$$ such that:

i) $$\forall a \in A$$, $$\exists b \in B$$ s.t. $$\rho(a,b) \leq \delta$$.

ii) $$\forall b \in B$$, $$\exists a \in A$$ s.t. $$\rho(a,b) \leq \delta$$.

Alternatively, suppose we denote by $$d(\cdot, C): M \rightarrow \mathcal{R}_{+}$$ the distance function for $$\forall x \in M$$ to the compact subset $$C \subseteq M$$ is $$\inf_{c \in C} \rho(x,c)$$.

$$Lemma(2.1)$$: 

$$
\begin{align*}
d_{H}(A, B) &= \max \left\{ \sup_{b \in B} d(b,A) , \sup_{a \in A} d(a,B) \right\}   (a)\\
&= \sup_{x \in M} |d(x,A) - d(x,B)|  (b)\\
&= ||d(\cdot, A) - d(\cdot, B)||_{\infty} (c)
\end{align*}
$$

$$proof$$: 

According to the definition 2.3, $$\sup_{b \in B} d(b,A) \geq $$ smallest $$\delta$$ satisfying ii) since for any $$b \in B$$, we can always pick $$a \in A$$ which satisfies $$\rho(b,a) = \inf_{a \in A} \rho(b,a) \leq \sup_{b \in B} d(b,A)$$. Similarly for i). Hence, $$d_{H}(A,B) \leq \left\{ \sup_{b \in B} d(b,A) , \sup_{a \in A} d(a,B) \right\}$$.

Conversely, we show that $$\sup_{b \in B} d(b,A) \leq $$ smallest $$\delta$$ satisfying ii), and similarly for i) by contradiction. Suppose not, 



 and similarly $$\sup_{a \in A} d(a,B)$$ satisfying i). 
(a) \rightarrow (b)



## 3. Covers


## 4. Simplicial Complexes



ref: 

