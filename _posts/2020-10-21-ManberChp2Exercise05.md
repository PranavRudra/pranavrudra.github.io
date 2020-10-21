---
layout: post
title: Exercise 2.05 (page 31)
category: solutions-manual
displayed: false
---

## Solution:

We will use constructive induction. First, we conjecture that for some $a, b, c, d \in \mathbb{R}$

$$
    \sum_{i = 1}^n i^2 = an^3 + bn^2 + cn + d
$$

For the base cases, consider $n = 0, 1, 2, 3$. 

$$
    \begin{alignat*}{3}
        \sum_{i = 1}^0 i^2 &= 0 &&= d \\
        \sum_{i = 1}^1 i^2 &= 1^2 = 1 &&= a + b + c \\
        \sum_{i = 1}^2 i^2 &= 1^2 + 2^2 =  5 &&= 8a + 4b + 2c \\
        \sum_{i = 1}^3 i^2 &= 1^2 + 2^2 + 3^2 =  14 &&= 27a + 9b + 3c
    \end{alignat*}
$$

Solving this system indicates

$$
    a = \frac{1}{3},\ b = \frac{1}{2},\ c = \frac{1}{6}
$$

For the inductive hypothesis (IH), assume

$$
    \sum_{i = 1}^{n - 1} i^2 = \frac{1}{3}(n - 1)^3 + \frac{1}{2}(n - 1)^2 + \frac{1}{6}(n - 1)
$$

Now, for the inductive step we have

$$
    \begin{align*}
        \sum_{i = 1}^n i^2 &= \left[ \sum_{i = 1}^{n - 1} i^2 \right] + n^2 \\
        &= \frac{1}{3}(n - 1)^3 + \frac{1}{2}(n - 1)^2 + \frac{1}{6}(n - 1) + n^2 \text{ (IH)} \\
        &= \frac{1}{3}n^3 + \frac{1}{2}n^2 + \frac{1}{6}n
    \end{align*}
$$

This simultaneously finds the desired formula and proves its correctness.

$$\qed$$