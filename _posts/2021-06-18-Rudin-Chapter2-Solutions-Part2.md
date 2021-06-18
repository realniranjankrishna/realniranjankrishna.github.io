---
title: Real Analysis Solutions (Rudin) - Chapter 2, Part 1
excerpt: "Real Analysis Solutions "
excerpt_separator: "<!--more-->"
categories:
  - Math
tags:
  - math
  - blog
  - analysis
  - rudin
mathjax: true
---

### Exercise 5
Construct a bounded set of real numbers with three limit points

*Proof:*
 
Consider the set $$S = (\{0 + \frac{1}{n}|n \in Z^{+}\} \cup \{1 + \frac{1}{n}|n \in Z^{+}\} \cup \{2 + \frac{1}{n}|n \in Z^{+}\}$$. This set has limit points $$L = \{1,2,3\}$$

### Exercise 6
Let $$E^{'}$$ be the set of all limit points of a set $$E$$. Prove that $$E^{'}$$ is closed. Prove that $$E$$ and $$\bar{E}$$ have the same limit points. Do $$E$$ and $$E^{'}$$ have the same limit points?

*Proof:*  
1. Assume $$E^{'}$$ is not closed. That means there exists a limit point $$p$$ of $$E^{'}$$ such that for any $$r > 0$$, there exists a point $$q \in N_{r}(p) \cap E$$ where t$$q \in E^{'}$$ and $$p \not\in E^{'}$$. This implies that $$p$$ is a limit point of $$\bar{E}$$ because $$\bar{E} = E \cup E^{'}$$. Since $$\bar{E}$$ is closed, $$p \in E$$ or $$p \in E^{'}$$. If $$p \in E^{'}$$, we have contradicted our inital assumption and the statement has been proven. Otherwise, we know that $$d(p,q) < r$$. Let $$h$$ be the real number such that $$d(p,q) = r - h$$. Select $$p^{'} \in E$$ such that $$d(q,p^{'}) < h$$. Then we know that $$d(p,p^{'}) \leq d(p,q) + d(q,p^{'}) < r  -h + h < r$$. Hence $$p$$ is a limit point of $$E$$. This implies that $$p \in E^{'}$$. This is a contradiction. Hence proved.
2. Every limit point $$p$$ of $$E$$ is in $$E^{'}$$. Since $$E^{'}$$ is close every limit point $$p$$ of $$E^{'}$$ is in $$E^{'}$$. Assume there exists a limit point $$p^{'}$$ of $$\bar{E}$$ that is not in $$E^{'}$$. That means for every real $$r > 0$$, there exists a point $$q \in \bar{E}$$ such that $$q \in N_{r}(p^{'}) \cap \bar{E}$$, Either $$q \in E$$ or $$q \in E^{'}$$. If $$q \in E$$, by definition it is a limit point of $$E$$, This implies that $$q \in E^{'}$$. This is a contradiction. The $$E^{'}$$ case can be proved similarly.
3. No. Consider the set  $$S = \{\frac{1}{n}|n \in Z^{+}\}$$. This has the limit point $$L = \{0\}$$. But $$L$$ has no limit points. Hence proved.

### Exercise 7
Let $$A_{1},A_{2},A_{3},...$$ be subsets of a metric space
1. If $$B_{n} = \cup^{n}_{i=1}A_{i}$$, prove that $$\bar{B_{n}} = \cup^{n}_{i=1}\bar{A_{i}}$$
2. If $$B = \cup^{\infty}_{i=1}A_{i}$$, prove that $$\cup^{\infty}_{i=1}\bar{A_{i}} \subset \bar{B} $$

Show, by an example, that this inclusion can be proper

*Proof:*
1. $$\bar{B_{n}} = B_{n} + B^{'}_{n} = \cup^{n}_{i=1}A_{i} + \cup^{n}_{i=1}A^{'}_{i}= \cup^{n}_{i=1}(A_{i} \cup A_{i}^{'}) = \cup^{n}_{i=1}\bar{A_{i}}$$. We know that $$B_{n} = \cup^{n}_{i=1}A_{i} $$. Hence we just need to prove that $$B^{'}_{n} = \cup^{n}_{i=1}A^{'}_{i}$$. 
Let $$p$$ be a limit point of $$B_{n}$$. Hence for every real $$r > 0$$ there exists a point $$q \in N_{r}(p) \cap B_{n}$$ such that $$q \in B_{n}$$. If $$q \in B_{n}$$, it means that $$q \in A_{\alpha}$$ for some $$\alpha$$.  Hence for every real $$r > 0$$ there exists a point $$q \in N_{r}(p) \cap A_{\alpha}$$ such that $$q \in A_{\alpha}$$. This implies that every $$p \in B^{'}_{n}$$ is in $$\cup^{n}_{i=1}A^{'}_{i}$$. Hence $$B^{'}_{n} \subset \cup^{n}_{i=1}A^{'}_{i}$$. Consider the reverse direction, Let $$p$$ be a limit point of some $$A_{\alpha}$$.Hence for every real $$r > 0$$ there exists a point $$q \in N_{r}(p) \cap A_{\alpha}$$ such that $$q \in A_{\alpha}$$. This implies that $$q \in B^{'}_{n}$$. Since $$\alpha$$ was arbitrary, every limit point of every $$A_{\alpha}$$ where $$\alpha \in n$$ is in $$B^{'}_{n}$$. Hence   $$ \cup^{n}_{i=1}A^{'}_{i} \subset B^{'}_{n}$$. Both of these conditions imply that $$B^{'}_{n} = \cup^{n}_{i=1}A^{'}_{i}$$
2. This is similar as $$(1)$$

Let $$S = \{\frac{1}{n}|n \in Z^{+}\}$$. Consider $$B = \cup^{\infty}_{i = 1}(i + S)$$

### Exercise 8
Is every point of every open set $$E \subset R^{2}$$ a limit point of $$E$$? Answer the same question for closed sets in $$R^{2}$$?

*Proof:*
1. Consider a point $$p \in E$$. Since $$E$$ is open, $$p$$ is an interior point of $$E$$. Then there exists $$N_{r}(p) \subset E$$ for some $$r > 0$$. Since $$N_{r}(p) \subset R^{2}$$ is infinite, we can say that it's a limit point of $$E$$.
2. Consider the set $$\{x_{0}\}$$


### Exercise 9
Let $$E^{0}$$ denote the set of all interior points of a set $$E$$.
1. Prove that $$E^{0}$$ is always open
2. Prove that $$E$$ is open if and only if $$E^{0} = E$$
3. If $$G \subset E$$ and $$G$$ is open. prove that $$G \subset E^{0}$$
4. Prove that the complement of $$E^{0}$$ is the closure of the complement of $$E$$.
5. Do $$E$$ and $$\bar{E}$$ always have the same interiors?
6. Do $$E$$ and $$\bar{E}$$ always have the same closures?

*Proof:*
1. For every $$p \in E^{0}$$ there exists an $$r > 0$$ such that $$q \in N_{r}(p) \cap E$$ where $$q \in E$$. Let $$d(p,q) = r - h$$. Then $$d(q,r) < h$$. By the triangle inequality we get $$d(p,r) \leq d(p,q) + d(q,r) < r -h+h < r$$. Hence $$r \in E^{0}$$
2. If $$E$$ is open every interior point of $$E$$ is in $$E$$. Therfore $$E^{0} = E$$. To prove the other direction, note that $$E^{0}$$ is always open. Therefore if $$E^{0} = E$$, we can see that $$E$$ is open as well.
3. If $$G \subset E$$ and $$G$$ is open, for every $$p \in G$$, there is a $$r > 0$$ such that $$N_{r}(p) \subset G \implies N_{r}(p) \subset E \implies p \in E^{0}$$. Since $$p$$ is any arbitrary point, this implies that $$G \subset E^{0}$$
4. We'll show that $${E^{0}}^c \subseteq \bar{E^{c}}$$ and vice versa. Let $$x \in  {E^{0}}^c \implies x \not\in E^{0}$$. This means there doesn't exist $$r > 0$$ such that $$N_{r}(x) \subseteq E \implies$$ for every $$r > 0$$ $$N_{r}(x) \cap E^{c} \neq \varnothing \implies x \in \bar{E^{c}}$$ . Let's show the other direction. Consider $$x \in \bar{E^{c}}$$. For every $$r > 0$$, $$N_{r}(x) \cap E^{c} \neq \varnothing \implies x \not\in E^{0} \implies x \in {E^{0}}^{c}$$ 
5. Consider $$E = Q$$ in $$R$$. Then $$E^{0} = \varnothing$$ and $$\bar{E}^{0} = R$$
6. Consider $$E = Q$$ in $$R$$. Then $$\bar{E} = R$$ and $$E^{0} = \varnothing \implies \bar{E^{0}} = \varnothing$$
