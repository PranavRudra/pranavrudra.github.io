---
layout: post
title: Exercise 2.01 (page 31)
category: solutions-manual
displayed: false
---

## Solution:

We will prove the following by induction on $n$.

$$
    x^n - y^n = (x - y)\left(\sum_{i = 0}^{n - 1}x^{n - 1 - i}y^{i} \right)
$$

Rewriting $x^n - y^n$ in this form $\forall n \in \mathbb{Z}^{\geq 1}$ constructively shows that $(x - y) \mid (x^n - y^n)$. That is, it gives a $c \in \mathbb{Z}$ such that $c(x - y) = x^n - y^n$. For the base case $(n = 1)$, observe that $x^1 - y^1 = (x - y)$. For the inductive hypothesis (IH), assume that the formula holds for $n - 1$. Now, for the inductive step, we have

$$
    \begin{align*}
        (x - y)\left(\sum_{i = 0}^{n - 1}x^{n - 1 - i}y^{i} \right) &= (x - y)\left(y^{n - 1} + \sum_{i = 0}^{n - 2}x^{n - 1 - i}y^{i} \right) \\
        &= (x - y)\left(y^{n - 1} + x\sum_{i = 0}^{n - 2}x^{n - 2 - i}y^{i} \right) \\
        &= (x - y)\left(y^{n - 1} + x\left[\frac{x^{n - 1} - y^{n - 1}}{x - y}\right] \right) \text{ (IH)} \\
        &= (x - y)y^{n - 1} + x(x^{n - 1} - y^{n - 1}) = x^n - y^n
    \end{align*}
$$

$$\qed$$