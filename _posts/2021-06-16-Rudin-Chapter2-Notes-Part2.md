---
title: Real Analysis Notes (Rudin) - Chapter 2, Part 2
excerpt: "Real Analysis Notes "
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

## Metric Spaces
**Definition:** A set $$X$$, whose elements we shall call points, is said to be a metric space if with any two points $$p$$ and $$q$$ of $$X$$ there is associated a real numer $$d(p,q)$$, called the distance from $$p$$ to $$q$$, such that
1. $$d(p,q) > 0$$ if $$ p\neq q; d(p,p) = 0 $$
2. $$d(p,q) = d(q,p)$$
3. $$d(p,q) \leq d(p,r) + d(r,q)$$, for any $$r \in X$$

Any function with these three properties is called a distance function or a metric.

**Definition:** We call a set $$E \subset R^{k}$$ convex if $$\delta x + (1-\delta)y \in E$$ whenever $$x,y \in E$$ and $$0 < \delta < 1$$

**Definition:** Let $$X$$ be a metric space. All points and sets mentioned below are understood to be elements and subsets of $$X$$.
1. A neighborhood of $$p$$ is a set $$N_{r}(p)$$ consisting of all $$q$$ such that $$d(p,q) < r$$, for some $$ r > 0$$, The number $$r$$ is called the radius $$N_{r}(p)$$.
2. A point $$p$$ is a limit point of the set $$E$$ if every neighborhood $$p$$ contains a point $$q \neq p$$ such that $$q \in E$$
3. If $$p \in E$$ and $$p$$ is not a limit point of $$E$$, then $$p$$ is called an isolated point of $$E$$.
4. $$E$$ is closed if every limit point of $$E$$ is a point of $$E$$.
5. A point $$p$$ is an interior point of $$E$$ if there is a neighborhood $$N$$ of $$p$$ such that $$N \subset E$$
6. The complement of $$E$$ (denoted by  $$E^{c}$$) is the set of all points $$ p \in X$$ and $$p \not\in E$$
7. $$E$$ is perfect if $$E$$ is closed and every point of $$E$$ is a limit point of $$E$$.
8. $$E$$ is bounded if there is a real number $$M$$ and a point $$q \in X$$ such that $$d(p,q) < M$$ for all $$p \in E$$
9. $$E$$ is dense in $$X$$ if every point of $$X$$ is a limit point of $$E$$ or a point of $$E$$ (or both)

**Theorem 2.19:** Every neighborhood is an open set

*Proof:* Consider a neighborhood $$E = N_{r}(p)$$ and let $$q$$ be any point in $$E$$. Since $$d(p,q) < r$$, there is a real number $$h$$ such that $$d(p,q)+h = r \implies d(p,q) = r - h$$. Consider the neighbourhood $$E^{'} = N_{h}(q)$$ and all points $$s$$ in this neighborhood. Note that $$d(q,s) < h$$. Then
$$d(p,s) \leq d(p,q) + d(q,s) < r - h + h = r \implies s \in E$$.
This means that $$N_{h}(q) \subset E$$. Hence $$q$$ is an interior point of $$E$$.

**Theorem 2.20:** If $$p$$ is a limit point of set $$E$$, then every neighborhood of $$p$$ contains infinitely many points of $$E$$.

*Proof:* Suppose there is a neighborhood $$N$$ of $$p$$ such that it only contains finite number of points $$q \in E$$. Let $$q_{1},q_{2},...,q_{n}$$ be such $$n$$ points. Consider $$r = \min(d(p,q_{1}),d(p,q_{2}),...,d(p,q_{n}))$$. Then the neighborhood $$N_{r}(p)$$ contains no point of $$q \in E$$ such that $$q \neq p$$. Hence $$p$$ is not a limit point of $$E$$ contradicting our initial assumptions.

**Corollary:** A finite point set has no limit points

*Proof:* This follows directly from Theorem 2.20

**Theorem 2.22:** Let $$\{E_{\alpha}\}$$ be a (finite or infinte) collection of sets $$E_{\alpha}$$. Then $$(\cup_{\alpha}E_{\alpha})^{c} = \cap_{\alpha}(E_{\alpha}^{c})$$

*Proof:* Let $$A$$ and $$B$$ be the left and right hand sides of the equation. If $$x \in A \implies x \not\in \cup_{\alpha}E_{\alpha} \implies x \not\in E_{\alpha} \text{ for any } \alpha \implies x \in E_{\alpha}^{c} \text{ for every } \alpha  \implies x \in \cap_{\alpha}E^{c}_{\alpha} \implies A \subset B$$.  If $$x \in B \implies x \in E^{c}_{\alpha} \text{ for every } \alpha \implies x \not\in E_{\alpha} \text{ for any} \alpha \implies x \not\in \cup_{\alpha}E_{\alpha} \implies x \in (\cup_{\alpha}E_{\alpha})^{c} \implies B \subset A$$. These two conditions imply that $$A = B$$.

**Theorem 2.23:** A set E is open if and only if its complement is closed

*Proof:* First assume that $$E^{c}$$ is closed. Choose $$x \in E \implies X \not\in E^{c} \implies x \text{ is not a limit point of } E^{c}$$. Hence there exists a nerighborhood $$N$$ of $$x$$ such that $$E^{c} \cap N = \{\varnothing\} \implies N \subset E$$. Hence $$x$$ is an interior point of $$E$$ and $$E$$ is open.
Assume that $$E$$ is open. Let $$x$$ be a limit point of $$E^{c}$$. Then every neighborhood of $$x$$ contains some $$q \in E^{c}$$, so that $$x$$ is not an interior point of $$E$$. Since $$E$$ is open, $$x \in E^{c}$$. Hence $$E^{c}$$ is closed.

**Corollary"** A set F is closed if and only if its complement is open

**Theorem 2.24:** 
1. For any collection $$\{G_{\alpha}\}$$ of open sets $$\cup_{\alpha}G_{\alpha}$$ is open.
2. For any collection $$\{F_{\alpha}\}$$ of closed sets $$\cap_{\alpha}F_{\alpha}$$ is closed.
3. For any finite collection $$G_{1},...,G_{n}$$ of open sets, $$\cap_{i=1}^{n}G_{i}$$ is open.
4. For any finite collection $$F_{1},...,F_{n}$$ of closed sets, $$\cap_{i=1}^{n}F_{i}$$ is closed.

*Proof:* Let $$G = \cup_{\alpha}G_{\alpha}$$. If $$x \in G \implies x \in G_{\alpha} \text{ for some } \alpha$$. Since $$G_{\alpha}$$ is open, $$x$$ is an interior point of it. Then it is also an interior point of $$G$$. Hence $$G$$ is open.
By Theorem 2.22, we have $$(\cap_{\alpha}F_{\alpha})^c = \cup_{\alpha}(F^{c}_{\alpha})$$. Since every $$F_{\alpha}$$ is closed, every $$F^{c}_{\alpha}$$ is open by Theorem 2.23. This implies that $$\cup_{\alpha}(F^{c}_{\alpha})$$ is open. Applying theorem 2.23 again we get that the $$\cap_{\alpha}F_{\alpha}$$ is closes as it is the complement of $$\cup_{\alpha}(F^{c}_{\alpha})$$.
Let $$H = \cap_{i=1}^{n}G_{i}$$. For any $$x \in H$$, there exists neighborhoods $$N_{i}$$ with radius $$r_{i}$$ such that $$N_{i} \subset G_{i}$$. Let $$r = \min(r_{1},r_{2},...,r_{n})$$ and let $$N$$ be the neighborhood of $$x$$ with radius $$r$$. Then $$N \subset G_{i}$$ for $$i = 1,2,...,n $$. This implies that $$N \subset H$$ and $$H$$ is open.
By the same reasoning for $$(2)$$, $$(4)$$ follows ffrom $$(3)$$.

**Definition:** If $$X$$ is a metric space, if $$E \subset X$$ , and if $$E^{'}$$ denotes the set of all limit points of $$E$$ in $$X$$, then the closure of $$E$$ is the set $$\bar{E} = E \cup E^{'}$$

**Theorem 2.27:** If $$X$$ is a metric space and $$E \subset X$$, then
1. $$\bar{E}$$ is closed
2. $$E = \bar{E}$$ if and only if $$E$$ is closed
3. $$\bar{E} \subset F$$ for every closed set $$F \subset X$$ such that $$E \subset F$$
Note that by $$(1)$$ and $$(3)$$, $$\bar{E}$$ is the smallest closed subset of $$X$$ that contains $$E$$.

*Proof:*
1. Let $$p \in X$$ and $$p \not\in \bar{E} \implies p \text{ not a limit point nor a point of } E$$. This means that $$p$$ has a neighborhood $$N$$ such that $$N \cap E = \{\varnothing \}$$. This implies that $$N$$ lies in $$(\bar{E})^c$$. Since $$p$$ is any arbritrary point, this means that $$(\bar{E})^c$$ is open. Therfore $$\bar{E}$$ is closed.
2. If $$\bar{E} = E$$ then $$E$$ is closed by $$(1)$$. If $$E$$ is closed, $$E^{'} \subset E \implies \bar{E} = E \cup E^{'} = E$$. Hence proved.
3. If $$F$$ is closed and $$E \subset F \implies F^{'} \subset F \implies E^{'} \subset F \implies \bar{E} \subset F $$ 

**Theorem 2.28:** Let $$E$$ be a nonempty set of real numbers which is bounded above. Let $$y = \sup E$$. Then $$y \in \bar{E}$$. Hence $$y \in E$$, if $$E$$ is closed.

*Proof:* If $$y \in E \implies y \in \bar{E}$$. Assume $$y \not\in E$$. For every $$h > 0$$ there exists an $$x \in E$$ such that $$y - h < x < y$$. If not $$y - h$$ would be an upper bound of $$E$$. Therefore $$x \in N_{h}(y)$$. Hence $$y$$ is a limit point of $$E$$. Therfore it is in $$\bar{E}$$

**Definition:** Suppose $$E \subset Y \subset X$$, where $$X$$ is a metric space. To say that $$E$$ is an open subset of $$X$$ means that to each point $$p \in E$$ there is associated a positive number $$r$$ such that $$d(p,q) < r, q \in X \implies q \in E$$. We say that $$E$$ is open relative to $$Y$$ if to each $$p \in E$$ there is an $$r > 0$$ such that $$q \in E$$ whenever $$d(p,q) < r$$ and $$q \in Y$$

**Theorem 2.30:** Suppose $$Y \subset X$$. A subset $$E$$ of $$Y$$ is open relative to $$Y$$ if and only if $$E = Y \cap G$$ for some open subset $$G$$ of $$X$$

*Proof:*  Suppose $$E$$ is open relative to $$Y$$, To each $$p \in E$$ there is a $$r > 0$$ such that $$d(p,q) < r, q \in Y \implies q \in E$$. Let $$V_{p}$$ be the set of all $$q \in X$$ such that $$d(p,q)  < r$$, and let $$G = \cup_{p \in E}V_{p}$$. By theorem 2.19 and 2.24 $$G$$ is an open subset of $$X$$.
Since $$p \in V_{p}$$ for all $$p \in E$$ it is clear the $$E \subset G \cap Y$$
By our choice of $$V_{p}$$ we have $$V_{p} \cap Y \subset E$$ for all $$p \in E \implies G \cap Y \subset E \implies E = G \cap Y$$
Conversely, if $$G$$ is open in $$X$$ and $$E = G \cap Y$$, every $$p \in E$$ has a neighborhood $$V_{p} \in G$$ (Because $$G$$ is open and $$p \in G$$). This implies that $$V_{p} \cap Y \subset E$$. Thus $$E$$ is open relative to $$Y$$
