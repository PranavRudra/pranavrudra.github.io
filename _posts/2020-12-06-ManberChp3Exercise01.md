---
layout: post
title: Exercise 3.01 (page 56)
category: solutions-manual
displayed: false
---

## Solution:

Let $P(n)$ be a polynomial in $n$ of degree $k$. That is, 

$$P(n) = a_kn^k + a_{k - 1}n^{k - 1} + \cdots + a_1n + a_0$$ 

where $k \in \mathbb{N}$ and $a_i \in \mathbb{R}^{\geq 0}$ for $i = 0, 1, 2, \ldots, k$. Also, let 

$$Q(n) = \left[1 + \left( \sum_{i = 0}^{k} a_i \right) \right] n^{k!}$$

$\forall n \geq 1$, clearly $0 \leq P(n) \leq Q(n)$. Thus, for all $n \geq 1$ and $b \in \mathbb{R}^+$

$$
    \begin{align*}
        \\
        \log_b(P(n)) &\leq \log_b(Q(n)) \\
        &= \log_b \left( \left[1 + \left( \sum_{i = 0}^{k} a_i \right) \right] n^{k!} \right) \\
        &= \log_b \left( \left[1 + \left( \sum_{i = 0}^{k} a_i \right) \right] \right) + k!\log_b(n) \\
        &\leq \left[ \log_b \left( \left[1 + \left( \sum_{i = 0}^{k} a_i \right) \right] \right)k! \right]\log_b(n) \\
        &= O(\log(n))
    \end{align*}
$$