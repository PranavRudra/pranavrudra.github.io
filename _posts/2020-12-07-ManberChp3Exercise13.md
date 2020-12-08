---
layout: post
title: Exercise 3.13 (page 57)
category: solutions-manual
displayed: false
---

## Solution:

Note that $\forall k > 0$, $f(i) = i^k$ is a monotonically increasing function. Hence, by $(3.34)$

$$
    \sum_{i = 1}^n i^k \leq \int_{x = 1}^{n + 1} x^k dx = \left[ \frac{x^{k + 1}}{k + 1} \right]_{1}^{n + 1} = \frac{(n + 1)^{k + 1} - 1}{k + 1} \leq (k + 100)!(n^{k + 1})
$$

Since $(k + 100)!$ is a constant, we have

$$
    \sum_{i = 1}^n i^k = O(n^{k + 1})
$$

$$\qed$$