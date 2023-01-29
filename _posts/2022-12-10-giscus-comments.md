---
layout: distill
title: TDA Notes(1)
date: 2023-01-28 11:59:00-0400
description: Pipeline, Metric Spaces, Covers, and Simplicial Complexes
categories: learning-notes data-analysis
giscus_comments: true


authors:
  - name: Xuanzhou Chen
    url: 
    affiliations:
      name: Home

bibliography: 2018-12-22-distill.bib


# Optionally, you can add a table of contents to your post.
# NOTES:
#   - make sure that TOC names match the actual section names
#     for hyperlinks within the post to work correctly.
#   - we may want to automate TOC generation in the future using
#     jekyll-toc plugin (https://github.com/toshimaru/jekyll-toc).
toc:
  - name: TDA Pipeline
    # if a section has subsections, you can add them as follows:
    # subsections:
    #   - name: Example Child Subsection 1
    #   - name: Example Child Subsection 2
  - name: Metric Space
  - name: Covers
  - name: Simplicial Complexes
  
# Below is an example of injecting additional post-specific styles.
# If you use this post as a template, delete this _styles block.
_styles: >
  .fake-img {
    background: #bbb;
    border: 1px solid rgba(0, 0, 0, 0.1);
    box-shadow: 0 0px 4px rgba(0, 0, 0, 0.1);
    margin-bottom: 12px;
  }
  .fake-img p {
    font-family: monospace;
    color: white;
    text-align: left;
    margin: 12px 0;
    text-align: center;
    font-size: 16px;
  }
---

## 1. TDA Pipeline
    1. The input is assumed to be a finite set of points with a notion of distance - or similarity - between them. The distance can be 1) induced by the metric in the ambient space(e.g. 2D? 3D?) or 2) an intrinsic metric defined by a pairwise distance matrix.
    2. 

## 2. Metric Space

$$\textbf{Def 2.1 Metric Space}$$: A metric space ($$M$$, $$\rho$$) is a set $$M$$ with a function $$\rho : M \times M \rightarrow \mathcal{R}_{+}$$, such that $$ \forall x, y, z \in M$$, the following is the case:

i) (Positivity) $$ \rho(x,y) \geq 0$$ and $$\rho(x,y) = 0$$ iff $$x = y$$.

ii) (Symmetry) $$\rho(x,y) = \rho(y,x)$$

iii) (The Triange Inequality) $$\rho(x,z) \leq \rho(x,y) + \rho(y,z)$$

$$\textbf{Def 2.2 Compact Subset}$$: A subset $$S \subseteq R$$ is called compact if every sequence in $$S$$ has a subsequence that converges to a point in $$S$$.

$$\textbf{Def 2.3 Hausdorff Distance}$$: Given two compact subsets $$A, B \subseteq M$$, the Hausdorff distance $$d_{H}(A,B)$$ between set $$A$$ and set $$B$$ is the smallest nonnegative number $$\delta$$ such that:

i) $$\forall a \in A$$, $$\exists b \in B$$ s.t. $$\rho(a,b) \leq \delta$$.

ii) $$\forall b \in B$$, $$\exists a \in A$$ s.t. $$\rho(a,b) \leq \delta$$.

Alternatively, suppose we denote by $$d(\cdot, C): M \rightarrow \mathcal{R}_{+}$$ the distance function for $$\forall x \in M$$ to the compact subset $$C \subseteq M$$ is $$\inf_{c \in C} \rho(x,c)$$.

$$Lemma(2.1)$$: 

$$
\begin{align*}
d_{H}(A, B) &= \max \left\{ \sup_{b \in B} d(b,A) , \sup_{a \in A} d(a,B) \right\}  \quad\quad (a)\\
&= \sup_{x \in M} |d(x,A) - d(x,B)| \quad\quad (b)\\
&= ||d(\cdot, A) - d(\cdot, B)||_{\infty} \quad\quad (c)
\end{align*}
$$


Proof:

According to the definition 2.3, $$\sup_{b \in B} d(b,A) \geq $$ smallest $$\delta$$ satisfying ii) since for any $$b \in B$$, we can always pick $$a \in A$$ which satisfies $$\rho(b,a) = \inf_{a \in A} \rho(b,a) \leq \sup_{b \in B} d(b,A)$$. Similarly for i). Hence, $$d_{H}(A,B) \leq \left\{ \sup_{b \in B} d(b,A) , \sup_{a \in A} d(a,B) \right\}$$.

Conversely, we show that $$\sup_{b \in B} d(b,A) \leq $$ smallest $$\delta$$ satisfying ii), and similarly for i). Suppose not, then $$\exists b \in B$$ and $$a \in A$$ such that $$\rho(a,b) \geq \inf_{a \in A} \rho(a,b) = \sup_{b \in B} d(a,b) > $$ smallest $$\delta$$ satisfying ii), which is contradiction.

Hence, we have proved for (a) is the definition.  Q.E.D.



For some situations where different data sets issued from different ambient space, the notion of the Hausdorff distance can be generalized to the Gromov-Hausdorff distance for comparison of any pair of compact metric spaces.

$$\textbf{Def 2.4 Isometric}$$: Two metric spaces $$(M_{1}, \rho_{1})$$ and $$(M_{2}, \rho_{2})$$ are isometric if there exists a bijection $\phi$: $M_{1} \rightarrow M_{2}$ s.t. $$\rho_{2}(\phi(x), \phi(y)) = \rho_{1}(x,y)$$ for any $$x, y \in M_{1}$$.

$$\textbf{Def 2.5 The Gromov-Hausdorff Distance}$$: The Gromov-Hausdorff Distance $$d_{GH}(M_{1}, M_{2})$$ between two compact metric spaces is the infimum of $$r \in \mathcal{R}, r \geq 0$$, such that there exists a metric space $$(M_{1}, \rho)$$ and two compact subspaces $$C_{1}, C_{2} \subseteq M$$, isometric to $$M_{1}, M_{2}$$ s.t. $$d_{H}(C_{1}, C_{2}) \leq r$$.

## 3. Covers


## 4. Simplicial Complexes



ref: 

