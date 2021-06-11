---
title: Studying Rudin - Chapter 1 
excerpt: "Solutions and Proof outlines for Baby Rudin"
excerpt_separator: "<!--more-->"
categories:
  - Math
tags:
  - math
  - blog
mathjax: true
---
## Exercise 1.1
If $$r$$ is rational(r\neq 0), and $$x$$ is irrational, prove that $$r+x$$ and $$rx$$ are irrational.

*Proof:*
Assume $$r+x$$ is rational. Then $$r+x - r = x$$ is rational. This is a contradiction. Proceed similarly for $$rx$$

## Exercise 1.2
Prove that there is no rational number whose square is 12

*Proof:*
Assume $$m^2 = 12 = 4\cdot{}3 \implies m = 2*\sqrt{3}$$. Then use previous problem and the proof of $$\sqrt{2}$$ is irrational to prove this problem

## Exercise 1.3
Prove proposition 1.15

*Proof:*
Multiply both sides by $$z = \frac{1}{x}$$. Choose z appropriately in a similar way for following problems

## Exercise 1.4
Let $$E$$ be a nonempty subset of an ordered set; suppose $$\alpha$$ is a lower bound of $$E$$ and $$\beta$$ be an upper bound of $$E$$. Prove that $$\alpha \leq \beta$$

*Proof:*
By definition, $$\alpha \leq x$$  and $$x \leq \beta$$ for $$x \in E$$. This implies $$\alpha \leq \beta$$

## Exercise 1.5
Let $$A$$ be a nonempty set of real numbers which is bounded below. Let $$-A$$ be the set of all numbers $$-x$$, where $$x \in A$$. Prove that
$$\inf A = - \sup A$$


*Proof:*
Let $$\alpha = \inf A$$. By definition $$\alpha \leq x$$ for $$x \in A$$. Multiplying both by $$-1$$, we get that $$-\alpha \geq -x$$. This implies that $$-\alpha$$ is an upper bound of $$-A$$. We just have to prove that this is the least upper bound and we are done.\\
We know that there exists atleast one $$x^{'}$$ such that if $$\gamma > \alpha \implies \gamma > x^{'}$$ for $$ x^{'} \in A$$. Multiplying both by $$-1$$ we get $$-\gamma < -\alpha\implies -\gamma > -x^{'}$$for $$- x^{'} \in -A $$. This implies that $$-\alpha$$ is the least upper bound of $$-A$$. The result follows.

## Exercise 1.6
Fix $$ b>1$$
1. If $$m,n,p,q$$ are integers $$n > 0 , q > 0$$ and $$r = \frac{m}{n} = \frac{p}{q}$$, prove that
 $$(b^m)^\frac{1}{n} = (b^p)^\frac{1}{q}$$

2. Prove that $$b^{x+y} = b^xb^y$$ Iif $$x$$ and $$y$$ are rational
3. If $$x$$ is real, define $$B(x)$$ to be the set of all real numbers $$b^t$$, where $$t$$ is rational and $$t \leq x$$. Prove that
 $$b^r = \sup B(x)$$

where r is rational
4. Prove that $$b^{x+y} = b^xb^y$$ Iif $$x$$ and $$y$$ are real

*Proof:*
1. $$\frac{m}{n} = \frac{p}{q} \implies mq = pn$$. Put $$r^{'} = nq$$. Exponentiate through both ways and Use Theorem 1.21.
2. Let $$x = \frac{p}{q}$$ and $$y = \frac{a}{b}$$ where $$p,a,q,b$$ are integers. $$x+y = \frac{pb+qa}{qb}$$. We can use the fact that for integers $$b^(c+d) = b^c\cdot{}b^d$$ to find that $$b^{pb+qa} = b^{pb}b^{qa}$$. Then proceed by using the previous problem to prove that\\ $$(b^{pb+qa})^\frac{1}{qb} =(b^{pb}b^{qa})^\frac{1}{qb} $$
3. By definition $$r \geq t \in B(r)$$. It is an upper bound of the set $$B(r)$$. Let $$\alpha$$ be the least upper bound of the set $$B(r)$$. This implies that $$\alpha \geq t \in B(r)$$ Since both $$\alpha, r \in B(r) \implies \alpha \geq r$$ and $$r \geq \alpha \implies r = \alpha$$ 
4. Let $$r \leq x$$ and $$s \leq y$$ where $$x,y$$ are rationals. This implies that $$r+s \leq x+y$$. From this we have the following.\\

$$b^{x}b^{y} \geq b^{r}b^{s}$$\\
 $$ b^{r}b^{s} \geq b^{r+s}$$\\
 $$b^{x+y} \geq b^{r+s}$$\\

All of this implies that $$b^{x}b^{y} \geq b^{x+y}$$. Since it is an upper bound, we have to prove that it is the least upper bound to imply equality.\\
Assume there exists an upper bound $$\alpha$$ to the set $$B(x+y)$$ such that $$b^{x}b^{y} > \alpha \geq b^{r+s}$$. But we know that $$b^{x}b^{y} >  b^{r}b^{s} $$or $$ b^{x}b^{y} = b^{r}b^{s}$$.\\
If $$ b^{x}b^{y} = b^{r}b^{s}$$ is true, then $$b^{r}b^{s} > \alpha$$ which is contradiction as $$b^{r}b^{s} \in B(x+y)$$. Otherwise $$ b^{x}b^{y} > b^{r}b^{s}$$ and$$b^{x}b^{y} > \alpha$$. Subtracting we get $$0 > \alpha - b^{r}b^{s}$$ which is a contradiction as $$\alpha \geq b^{r}b^{s}$$. Hence proved


## Exercise 1.7
Fix $$b > 1, y > 0$$ and prove that there is a unique real $$x$$ such that$$b^x = y$$

*Proof:*
$$b^n - a^n = (b-a)(b^n-1+b^n-2a+...+a^n-1) \implies b^n - 1 \geq n(b-1)$$.\\
Put $$\frac{1}{n}$$ in the place of $$n$$ to get $$b - 1 \geq n(b^\frac{1}{n} - 1)$$\\
if $$t > 1$$ and $$n > \frac{b-1}{t-1} \implies n > \frac{n(b^\frac{1}{n} - 1)}{t-1} \implies b^\frac{1}{n} < t$$
Let $$t = y\cdot{}b^{-w} \implies b^\frac{1}{n} <  y\cdot{}b^{-w}\implies b^{w+\frac{1}{n}} <  y$$
Let $$t = y\cdot{}b^{-w} \implies b^\frac{1}{n} <  y\cdot{}b^{-w}\implies b^{w+\frac{1}{n}} <  y$$
Put $$-n$$ instead of $$n$$ and we can prove that next outline.
According to the two previous outlines if $$x = \sup A$$ we have $$b^{x+\frac{1}{n}} < y$$ and $$b^{x-\frac{1}{n}} > y$$ . This implies that $$x -\frac{1}{n}$$ is an upper bound of the set $$A$$. This contradicts our assumptions that $$x = \sup A$$. Thus $$b^x = y$$
Suppose there exists $$x,x^{'}$$ such that $$b^x = b^{x^{'}}$$. According to theorem 1.21 $$x = x^{'}$$. Hence proved.

## Exercise 1.8
Prove that no order can be defined in the complex field that turns it into an ordered field.

*Proof:*
Any $$x \neq 0$$ in an ordered field squared must be greater than 0. But $$i \neq 0$$ and $$i^2 = -1< 0$$. 


## Exercise 1.9
Suppose complex numbers are ordered using lexicographic order. Prove that this turns the set into of all complex numbers into an ordered set. Does this set have L.U.B?


*Proof:*
The first question is simply case work. As far as the second question goes,the fact that $$ib < i(b+1)$$ can be used here.

## Exercise 1.10
Suppose $$z = a+bi, w = u+vi$$, and

$$a = (\frac{\lvert  w  \rvert  + u}{2})^{\frac{1}{2}}$$ and $$b = (\frac{\lvert  w \rvert  - u}{2})^{\frac{1}{2}}$$

Prove that $$z^2 = w$$ if $$v \geq 0$$ and $$z\bar{z} = w$$ if $$w \leq 0$$. Conclude that every complex number (With one exception) has two complex square roots

*Proof:*
The first part is direct application of formula. The exception is 0.

## Exercise 1.11
If $$z$$ is a complex number, prove that there exists an $$r \geq 0$$ and a complex number $$w$$ such that $$\lvert w \rvert  = 1$$ such that $$z = rw$$. Are $$w$$ and $$r$$ uniquely determined by $$z$$.

*Proof:*
Let $$z = a +ib$$. Let $$w = c+id$$. We can choose $$c =\frac{a}{a+b} $$ and $$d = \frac{b}{a+b}$$ and $$r = a+b$$. Apart from the case $$z = 0$$, it is clear that $$w,r$$ are uniquely determined by $$z$$.

## Exercise 1.12
If $$z_{1},...,z_{n}$$ are complex, prove that

$$\lvert z_{1} + z_{2} + ... + z_{n} \rvert  \leq \lvert z_{1} \rvert  + \lvert z_{2} \rvert  + ... + \lvert z_{n} \rvert $$


*Proof:*
We'll use induction. For $$n=2$$, this is true according to Theorem 1.37. Assume it's true for all $$n$$.
Let $$z^{'} = z_{1}+...+z_{n}$$. We need to prove that\\

$$\lvert z_{'} + z_{n+1} \rvert  \leq \lvert z_{1} \rvert  + \lvert z_{2} \rvert  + ... + \lvert z_{n+1} \rvert $$\\

Applying Theorem 1.37 we get,  $$\lvert z_{'} + z_{n+1} \rvert  \leq\lvert z_{'} \rvert  +\lvert z_{n+1} \rvert $$. But we know from our induction hypothesis that $$\lvert z_{n+1} \rvert  \leq   \lvert z_{1} \rvert  + \lvert z_{2} \rvert  + ... + \lvert z_{n} \rvert $$. Substitute that and we're done.

## Exercise 1.13
If $$x,y$$ are complex, prove that

   $$ \lvert \lvert x \rvert  - \lvert y \rvert  \rvert  \leq \lvert x-y \rvert $$


*Proof:*
According to Theorem 1.37
   $$ \lvert x \rvert \leq \lvert x-y \rvert  + \lvert y \rvert  \implies \lvert x \rvert  - \lvert y \rvert  \leq \lvert x-y \rvert  $$\\
   Applying the theorem again \lvert x \rvert  - \lvert y \rvert   \leq \lvert x-y}$$


## Exercise 1.14
If $$\lvert z \rvert  = 1$$ and $$z\bar{z} = 1$$. compute

   $$ \lvert 1+z \rvert ^2 \leq \lvert 1-z \rvert ^2$$


*Proof:*
The answer is 4. It involves direct computation

## Exercise 1.15
It is clear that $$B(AB -\lvert C \rvert ^2) = 0$$ is when the equality holds. Then either $$b_{i} = 0,b_{i} \in B$$ or $$AB= \lvert C \rvert ^2 \implies (a_{1},a_{2},...,a_{n}) = \frac{C}{B}(b_{1},b_{2},...,b_{n})$$

## Exercise 1.16
Suppose $$k \geq 3,**x**,**y** \in R^k, \lvert x-y \rvert  = d > 0$$ and $$r > 0$$
1. If $$2r > d$$, there are infinitely main $$**z** \in R^k$$ such that

$$\lvert z-x \rvert  = \lvert z-y \rvert  = r$$

2. If $$2r > d$$, there is one $$**z**$$
3. If $$2r < d$$, there are no $$**z**$$


## Exercise 1.17
Prove that
$$\lvert x-y \rvert ^2 + \lvert x-y \rvert ^2 = 2\lvert x \rvert ^2 + 2\lvert y \rvert ^2$$ for $$x,y \in R^k$$



*Proof:*
The result directly follows from Theorem 1.37. Remember that $$(a+b)^2 + (a-b)^2 = 2a^2+2b^2$$

## Exercise 1.18
If $$k \geq 2$$ and $$**x** \in R^k$$, prove that there exists $$ **y** \in R^k$$ such that $$**y**\neq 0$$ but $$**x** \cdot{}**y** = 0$$. Is this true for $$k = 1$$?

*Proof:*
Let's prove this through induction.
For $$k=2 $$, $$**x** = (x_{1},x_{2})$$ we can select $$y = (x_{1},-\frac{x_{1}^2}{x_{2}})$$.
Assume true for all n, for $$n+1$$ We can take the sum of all previous dot products divided by $$x_{n+1}$$


## Exercise 1.19
Suppose $$**a** \in R^k, **b** \in R^k.$$ Find $$c \in R^k$$ and $$r > 0$$ such that

$$\lvert x-a \rvert  = 2\lvert x-b \rvert  $$

if and only if $$\lvert x-c \rvert  = r$$

*Proof:*
This involves direct computation.

## Exercise 1.20

