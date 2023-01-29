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

\textbf{Def 2.1}: A metric space ($$M$$, $$\rho$$) is a set $$M$$ with a function $$\rho : M \times M \rightarrow \mathcal{R}_{+}$$, such that $$ \forall x, y, z \in M$$, the following is the case:
i) (Positivity) $$ \rho(x,y) \geq 0$$ and $$\rho(x,y) = 0$$ iff $$x = y$$.
ii) (Symmetry) $$\rho(x,y) = \rho(y,x)$$
iii) (The Triange Inequality)$$\rho(x,z) \leq \rho(x,y) + \rho(y,z)$$

\textbf{Def 2.2}: A subset $$S \subseteq R$$ is called compact if every sequence in $$S$$ has a subsequence that converges to a point in $$S$$.

\textbf{Def 2.3}: Given two compact subsets $$A, B \subseteq M$$, the Hausdroff distance $$d_{H}(A,B)$$ between $$A$$ and 



## Covers


## Simplicial Complexes

