---
title: Math 38 SP20 Dartmouth Problem Set 1
excerpt: "Graph Theory Solutions "
excerpt_separator: "<!--more-->"
categories:
  - Math
tags:
  - math
  - blog
  - graph theory
  - dartmouth
mathjax: true
---
**Only questions that require proofs are done**
### 4
Prove or disprove:  The complement of a simple disconnected graph is connected.

*Proof.*

Consider a disconnected graph $$G$$. Let $$u,v \in G$$. Either there is no edge between $$u$$ and $$v$$ or there is an edge between $$u$$ and $$v$$. If the first case is true, $$uv$$ is an edge of $$\bar{G}$$ by definition of a complement.  Suppose there is an edge between $$u$$ and $$v$$. Since $$G$$ is disconnected there exists atleast two components to this graph. Consider some vertex $$w$$ in the any component other than the one containing $$u$$ and $$v$$. Then $$uw$$ and $$vw$$ are edges in $$\bar{G}$$. Then $$uwv$$ is a path in $$\bar{G}$$. Hence proved


### 5
Prove or disprove: In every group of six people, there are at least three mutual strangersor three acquaintances.

*Proof.*
Consider a graph $$K_{6}$$. Let's color the edges of it with either red or blue. Proving that it contains a red triangle or a blue triangle is similar to proving the actual question. Consider $$v \in G$$, since $$v$$ has $$5$$ neighbors, there is atleast three edges among them of the same color, let's say blue. Consider the $$3$$ vertices with blue edges connected to $$v$$. Either all edges connecting these $$3$$ vertices is all red,in which case we there is a red traingle, or there is on blue edge. In the latter case, we can consider the edge from the vertexc $$v$$ and create a blue triangle. Hence proved.
