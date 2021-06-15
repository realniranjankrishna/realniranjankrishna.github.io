---
title: Real Analysis Notes (Rudin) - Chapter 2, Part 1
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

## Finite, Countable and Uncountable Sets
**Definition:** For any positive integer $$n$$, let $$J_{n}$$ be the set whose elements, are the integers $$1,2,...,n$$; let $$J$$ be the set consiting of all positive integers. For any set $$A$$, we say
1. $$A$$ is finite if $$A \sim J_{n}$$ for some $$n$$. The empty set is also finite
2. $$A$$ is infinite if $$A$$ is not finite.
3. $$A$$ is countable if $$A \sim J$$
4. A is uncountable if $$A$$ is neither finite nor countable
5. A is at most countable if $$A$$ is finite or countable

**Definition:** By a sequence, we mean a function $$f$$ defined on the set $$J$$ of all positive integers. If $$f(n) = x_{n}$$, for $$n \in J$$, it is customary to denote the sequence $$f$$ by the symbol $$\{x_{n}\}$$ or $$x_{1},x_{2},x_{3},...$$. If $$A$$ is a set and if $$x_{n} \in A$$ for all $$n \in J$$, then $$\{x_{n}\}$$ is said to be a sequence in $$A$$ or a sequence of elements of $$A$$.

**Theorem 2.8:** Every infinite subset of a countable set $$A$$ is countable

*Proof:*  Suppose $$E \subset A$$ and $$E$$ is infinite. Arrange the elements $$x \in A$$ in a sequence of $$\{x_{n}\}$$ of distinct elements. Construct a sequence as follows.
Let $$n_{1}$$ be the smallest positive integers such that $$x_{n_{1}} \in E$$. Choose $$n_{1},...,n_{k-1}$$ ($$k = 1,2,3,...$$), let $$n_{k}$$ be the smallest integer greater than $$n_{k-1}$$ such that $$x_{n_{k-1}} \in E$$. Put $$f(k) = x_{n_k} (k=1,2,3,...)$$. It's clear that $$f(k) \sim J$$. Hence proved.

**Definition:** Let $$A$$ and $$\omega$$ be sets. and suppose that with each element $$\alpha \in A$$ there is associated a subset of $$\omega$$ which we denote by $$E_{\alpha}$$. The set whose elements are the set $$E_{\alpha}$$ will be denoted by $$\{E_{\alpha}\}$$. 
Then the union is defined as $$S  = \cup_{\alpha \in A} E_{\alpha}$$
The intersection is defined as $$S  = \cap_{\alpha \in A} E_{\alpha}$$

**Theorem 2.12:** Let $$\{E_{n}\}$$, $$n = 1,2,3,...,$$ be a sequence of coutnable sets and put $$S = \cup^{\infty}_{n=1}E_{n}$$. Then $$S$$ is countable

*Proof:*Let every set $$E_{n}$$ be arranged in a sequence $$\{x_{nk}\}$$.$$k = 1,2,3,...$$ and consider the infinite array

$$x_{11}\text{ }x_{12}\text{ }x_{13}\text{ }x_{14}\text{ }...$$ 

$$x_{21}\text{ }x_{22}\text{ }x_{23}\text{ }x_{24}\text{ }...$$ 

$$x_{31}\text{ }x_{32}\text{ }x_{33}\text{ }x_{34}\text{ }...$$ 

$$x_{41}\text{ }x_{42}\text{ }x_{43}\text{ }x_{44}\text{ }...$$ 

$$..........................$$

in which the elements of $$E_{n}$$ form the $$n$$th row. This can be arranged in sequence
$$x_{11};x_{12};x_{12};x_{31};x_{22};x_{13};x_{41};x_{32};x_{23};x_{14}$$.
If any two of the sets $$E_{n}$$ have elements in common, these will appear more than once here. There is a subset $$T$$ of the set of all positive integers such that $$S \sim T$$. which shows $$S$$ is atmost countable. Since $$E_{1} \subset S$$ and $$E_{1}$$ is infinite, $$S$$ is infinite and thus countable.

**Corollary:** Suppose $$A$$ is atmost countable, and, for every $$\alpha \in A$$, $$B_{\alpha}$$ is atmost countable. Put 
$$T = \cup_{\alpha \in A} B$$. Then $$T$$ is atmos countable.

*Proof:* Because $$T \subset S$$.

**Theorem 2.13** Let $$A$$ be a countable set, and let $$B_{n}$$ be the set of all n-tuples $$(a_{1},...,a_{n})$$ where $$a_{k}\in A (k = 1,...,n)$$ and the elements $$a_{1},...,a_{k}$$ need not be distinct. Then $$B_{n}$$ is countable

*Proof:*  It is clear that $$B_{1}$$ is countable as $$B_{1} = A$$. Suppose $$B_{n-1}$$ is countable $$(n = 2,3,4,...)$$. The elements of $$B_{n}$$ are of the form $$(b,a) \text{ }(b \in B_{n-1}, a\in A) $$
For every fixed $$b$$, the set of pairs $$(b,a)$$ is equivalent to $$A$$, and hence countable. Thus $$B_{n}$$ is the union of a countable set oc coutnable sets. By Theorem 2.12, $$B_{n}$$ is countable.

**Corollary:** The set of all rational numbers is countable

*Proof:* Apply theorem 2.13 with $$n=2$$. This is because every rational is of the form $$\frac{b}{a}$$ where $$a$$ and $$b$$ are integers. The set of pairs $$(a,b)$$ are then countable. This implies the set of fraction $$\frac{b}{a}$$ are countable.

**Theorem 2.14:** Let $$A$$ be the set of all sequences whose elements are the digits are $$0$$ and $$1$$. This set $$A$$ is uncountable.

*Proof:* Let $$E$$ be a countable subset of $$A$$, and let $$E$$ consist of the sequences $$s_{1},s_{2},s_{3},...$$. We construct a sequence $$s$$ as follows. If the $$n$$th digit in $$s_{n}$$ is $$1$$ then the $$n$$th digit in $$s$$ be $$0$$ and vice versa, Then the sequence differes from every member of $$E$$ in atleast one place; hence $$s \in E$$. But $$s \in A$$, so that $$E$$ is a proper subset of $$A$$.
Thus every countable subset of $$A$$ is a proper subset of $$A$$. This implies that $$A$$ is uncountable. If $$A$$ is countable, $$A$$ would be the proper subset of $$A$$ itself which cannot happen.
