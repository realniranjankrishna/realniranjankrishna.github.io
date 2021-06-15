---
title: Topology Notes (Munkres) - Chapter 2, Part 2
excerpt: "Topology notes "
excerpt_separator: "<!--more-->"
categories:
  - Math
tags:
  - math
  - blog
  - topology
  - munkres
  - notes
mathjax: true
---

## The Order Topology

**Definition:** Let $$X$$ be a set with a simple order relation; assume $$X$$ has more than one element. Let $$\\B$$ be the collection of all sets of the following types:
1. All open intervals $$(a, b)$$ in $$X$$.
2. All intervals of the form $$[a_{o}, b)$$, where ao is the smallest element (if any) of $$X$$.
3. All intervals of the form $$(a, b_{o}]$$, where bo is the largest element (if any) of $$X$$.
The collection $$B$$ is a basis for a topology on X, which is called the order topology.

*Proof:* Let's prove that $$B$$ is indeed a basis. Every element $$x \in X$$ either lies in
1. $$[a_{0},b)$$ (if it is the smallest element)
2. $$(a,b_{0}]$$ (if it is the largest element)
3. $$(a,b)$$ (if otherwise)

Hence, the first condition is satisified. Now we need to do some case work to prove the second condition. Let $$B = (a,b), B_{1} = [a_{0},b), B_{2} = (a,b_{0}]$$. Note that $$a_{0}$$ is the smallest element and $$b_{0}$$ is the largest element
*Case 1:* Assume $$x \in B_{2} \cap B_{1}$$
Then we can find a set $$B^{'} = (a_{0},b_{0})$$ such that $$x \in B^{'} \subset B_{1} \cap B_{2}$$
*Case 2:* Assume $$x \in B \cap B_{1}$$
Then we can find a set $$B^{'} = [a_{0},b)$$ of the form  such that $$x \in B^{'} \subset B \cap B_{1}$$

*Case 3:* Assume $$x \in B \cap B_{2}$$
Then we can find a set $$B^{'} = (a,b_{0}]$$ of the form  such that $$x \in B^{'} \subset B \cap B_{2}$$
*Case 4:* Assume $$x \in B \cap B_{3}$$ such that $$B_{3} = (a_{1},b_{1})$$
Then we can find a set $$B^{'} = (\max(a,a_{1}),\max(b,b_{1}))$$ of the form  such that $$x \in B^{'} \subset B \cap B_{2}$$
Therefore $$B$$ is a basis.

**Definition:** If $$X$$ is an ordered set, and $$a$$ is an element of $$X$$, there are four subsets of $$X$$ that are called the rays determined by a They are the following-
1. $$(a, +\infty) = \{x | x > a\}$$
2. $$(-\infty, a) = \{x | x < a\}$$
3. $$[a, +\infty) = \{x | x \geq a\}$$
4. $$(-\infty, a] =\{x | x \leq a\}$$

Sets of the first two types are called open rays, and sets of the last two types are called closed rays.
*Proof:* We'll show that open rays are open in the order topology and that they from a subbasis for the order topology on $$X$$.
If $$X$$ has a largest element, then $$(a,+\infty)$$ is equivalent to $$(a,b_{0}]$$. If not,$$(a,+\infty)$$ equals the union of all elements $$(a,x)$$ where $$x > a$$. Either way it is open in the order topology. Similar argument can be made for $$(-\infty,a)$$.
Since open rays are in the order topology, the topology that they generate is in the order topology as well. Furthermore, every basis element of the order topology equals a finite intersection of open rays. $$(a,b) = (-\infty,b) \cap (a,\infty)$$. The sets $$[a_{0},b)$$ and $$(a,b_{0}]$$ are open themeselves if they exist.
## The Product Topology on $$X \times Y$$

**Definition:** Let $$X$$ and $$Y$$ be topological spaces. The product topology on $$X \times Y$$ is the topology having as basis the collection $$B$$ of all sets of the form $$U \times V$$, where $$U$$ is an open subset of $$X$$ and $$V$$ is an open subset of $$Y$$.
*Proof:* Let's check if $$B$$ is a basis. The first condition is trivial as $$X \times Y \in B$$.
For the second condition consider sets $$U_{1} \times V_{1}$$ and $$U_{2} \times V_{2}$$
$$(U_{1} \times V_{1}) \cap (U_{2} \times V_{2}) = (U_{1} \cap U_{2}) \times (V_{1} \cap V_{2})$$. 

Since $$ (U_{1} \cap U_{2})$$ is open in $$X$$ and $$(V_{1} \cap V_{2})$$ is open in $$Y$$, by definition $$(U_{1} \cap U_{2}) \times (V_{1} \cap V_{2}) \in B$$

**Theorem 15.1:** If $$B$$ is a basis for the topology of $$X$$ and $$C$$ is a basis for the topology of $$Y$$, then the collection
$$D = \{B^{'} \times C^{'} |B^{'} \in B \text{ and } C^{'} \in C\}$$
is a basis for the topology of $$X \times Y$$ 
*Proof:* Given $$W \in X \times Y$$ and $$x \times y \in W$$, according to the definition of the product topology, there exists open sets $$U \in X$$ and $$V \in Y$$ such that $$ x \in U \times Y \subset W$$. Since $$B$$ is the basis for the topology of $$X$$, we can find $$B^{'} $$ such that $$x \in B^{'} \subset U$$. In a similar way we can find $$C^{'} $$ such that $$y \in C^{'}  \subset V$$. This implies that $$x \times y \in B^{'} \times C^{'} \subset W$$. Hence it is a basis according to Lemma 13.2.

**Definition:** Let $$\pi_{1} : X \times Y \to X$$ defined by the equation
$$\pi_{1}(x,y) = x$$ and
let $$\pi_{2} : X \times Y \to Y$$ defined by the equation
$$\pi_{2}(x,y) = y$$
The maps $$\pi_{1}$$ and $$\pi_{2}$$ are called the projections of $$X \times Y$$ onto its first and second factors, respectively.

If $$U$$ is an open subset of $$X$$, then the set $$\pi_{1}^{-1}(U)$$ is precisely the set $$U \times Y$$, which
is open in$$ X \times Y$$. Similarly, if $$V$$ is open in $$Y$$ then
$$\pi_{2}^{-1}(V) =  X \times V$$,

**Theorem 15.2:** The collection
$$S = \{\pi_{1}^{-1}(U) | U \text{ is open in } X\} \cup \{\pi_{1}^{-1}(V) | V\text{ is open in } Y\} $$
is a subbasis for the product topology on $$X \times Y$$.
*Proof:* Let $$T$$ denote the product topology on $$X \times Y$$, let $$T^{'}$$ be the topology generated by $$S$$. Since every $$s \in S \implies s \in T$$, arbitrary unions of finite intersection also belong in $$T$$. Hence $$T^{'} \subset T$$. On the other hand, every basis element  $$U \times V = \pi_{1}^{-1} \cap   \pi_{2}^{-1}$$.Therefore $$U \times V \in T^{'}$$. This implies that $$T \subset T^{'}$$. Hence proved. 

## The Subspace Topology

**Definition:** Let $$X$$ be a topological space with topology $$T$$. If $$Y$$ is a subset of $$X$$, the collection
$$T_{Y} = \{Y \cap U | U \in T\}$$
is a topology on $$Y$$, called the subspace topology. With this topology, $$Y$$ is called a subspace of $$X$$ its open sets consist of all intersections of open sets of $$X$$ with $$Y$$.
*Proof:* It is clear that $$\varnothing,Y \in T_{Y}$$ as $$\varnothing, X \in T$$. The fact that it is closed under arbitrary unions and finite intersections is clear from these equations.
$$(U_{1}\cap Y) \cap (U_{2} \cap Y) ... (U_{n} \cap Y) = (U_{1} \cap U_{2} ... U_{n}) \cap Y$$ 
$$\cup_{\alpha \in J} (U_{\alpha} \cap Y) = (\cup_{\alpha \in J} U_{\alpha}) \cap Y$$

**Lemma 16.1:** If $$B^{'}$$ is a basis for the topology of $$X$$ then the collection $$B_{Y} = \{B \cap Y | B \in B^{'}\}$$
is a basis for the subspace topology on $$Y$$
*Proof:* If $$U \in X$$ and $$y \in U \cap Y$$, then there is an element $$B \in B^{'}$$ such that $$y \in B \subset U$$. This implies that $$ y \in B \cap Y \subset U \cap Y  $$. By Lemma 13.2 this means that it is a basis.

**Lemma 16.2:** Let $$Y$$ be a subspace of $$X$$. If $$U$$ is open in $$Y$$ and $$Y$$ is open in $$X$$, then $$U$$ is open in $$X$$.
*Proof:* Let $$U$$ be open in $$Y$$. This implies that $$U = Y \cap V$$ where $$V$$ is open in $$X$$. By definition this implies that $$Y\cap V$$ is open in $$X$$.

**Theorem 16.3:** If $$A$$ is a subspace of $$X$$ and $$B$$ is a subspace of $$Y$$, then the product topology on $$A \times B$$ is the same as the topology $$A \times B$$ inherits as a subspace of $$X \times  Y$$.
*Proof:* The set $$U \times V$$ is the general basis in $$X \times Y$$. Therefore $$(U \times V) \cap (A \times B)$$ is the general basis element of $$A \times B$$.
$$(U \times V) \cap (A \times B) = (U \cap A) \times (V \cap B)$$
Since $$U \cap A$$ and $$V \cap B$$ are the general open sets for the subspace topologies on $$A$$ and $$B$$, respectively, the set $$ (U \cap A) \times (V \cap B)$$ is the general basis element for the product topology on $$A \times B$$. Hence the bases are same. Hence the topologies are same.

**Definition:**Given an ordered set $$X$$, let us say that a subset $$Y$$ of $$X$$ is convex in $$X$$ if for each pair of points $$a < b$$ of $$Y$$, the entire interval $$(a, b)$$ of points of $$X$$ lies in $$Y$$

**Theorem 16.4:** Let $$X$$ be an ordered set in the order topology; let $$Y$$ be a subset of $$X$$ that is convex in $$X$$ Then the order topology on $$Y$$ is the same as the topology $$Y$$ inherits as a subspace of $$X$$.
*Proof:*
Consider the open ray $$(a,+\infty)$$. If $$a \in Y$$, $$a \cap Y = \{x \in Y | x > a\}$$ this is an open ray of the ordered set $$Y$$. If $$a \not\in Y$$, then it's either the upper bound or lower bound of $$Y$$. In the former case $$(a, +\infty) \cap Y$$ equals all of Y and the latter it is empty.
By simialr reasoning it shows that $$(-\infty,a) \cap Y$$ is either an open ray of $$Y$$, or $$Y$$ itself or empty. Since the sets $$(a, +\infty)\cap Y$$ and $$ (-\infty,a) \cap Y $$ form a subbasis for the subspace topology on $$Y$$, and since each is open in the order topology, the order topology contains the subspace topology.
To prove the reverse, any open ray of $$Y$$ equals an intersection of an open ray of $$X$$ with $$Y$$. Since the open rays of $$Y$$ are a subbasis for the order topology on $$Y$$, this topology is contained in the subspace topology.
