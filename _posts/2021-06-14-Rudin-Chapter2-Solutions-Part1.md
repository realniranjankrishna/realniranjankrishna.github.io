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

### Exercise 1
Prove that the empty set is a subset of every set

*Proof:* Assume otherwise. Then for an arbitrary set $$A$$, $$\{\varnothing\} \cap A \ = \{\varnothing\}$$ by defintion of an empty set. But this also implies $$\{\varnothing\} \in A$$. This contradicts our inital assumption.

### Exercise 2
A complex number $$z$$ is said to be algebraic if there are integers $$a_{0},...,a_{n}$$ not all zero, such that
$$a_{0}z^n + a_{1}z^{n-1} +...+a_{n-1}z+a_{n} = 0$$.
Prove that the set of all algebraic numbers is countable

*Proof:* Consider set $$S = \{ a_{0},a_{1},...,a_{n}\}$$. This is clearly countable. Now consider $$a_{0}z^n + a_{1}z^{n-1} +...+a_{n-1}z+a_{n} = 0$$. This equation can have atmost $$n$$ solutions. The solutions $$z$$ depends on the degree $$n$$ of the polynomial and the set $$S$$. So every $$z$$ can be identified by the set $$S^{'} = \{a_{1},a_{2},...,a_{n},n\}$$. This is also countable as $$n$$ is an integer. Then $$Z = \cup S^{'}$$. By theorem 2.12 this is also countable. Hence proved.

### Exercise 3
Prove that there exist real numbers which are not algebraic

*Proof:* Assume all real numbers are algebraic. Then $$R$$ can be represented by $$\cup S_{z}$$ which is countable. But $$R$$ is not countable. This is a contradiction. Hence proved.

### Exercise 4
Is the set of all irrational real numbers countable?

*Proof:*
The set of irrational numbers can be represented by $$R \backslash Q$$ where $$Q$$ represents the rational numbers. Assume $$R  \backslash Q$$ is countable. By theorem 2.12 $$ (R \backslash Q) \cup Q$$ is countable. This is equal to $$R$$ which is uncountable. This is a contradiction. Hence proved.
