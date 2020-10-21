---
layout: post
title: Exercise 2.03 (page 31)
category: solutions-manual
displayed: false
---

## Solution:

We will use induction. First, we conjecture (using some familiar formulas) that

$$
    \sum_{i = 1}^n i(i + 1) = \sum_{i = 1}^n i^2 + \sum_{i = 1}^n i = \frac{n(n + 1)(2n + 1)}{6} + \frac{3n(n + 1)}{6} = \frac{n(n + 1)(n + 2)}{3}
$$

For the base case, consider $n = 1$. Clearly,

$$
     \sum_{i = 1}^1 i(i + 1) = 1(2) = 2 = \frac{1(2)(3)}{3}
$$ 

For the inductive hypothesis (IH), assume

$$
    \sum_{i = 1}^{n - 1} i(i + 1) = \frac{(n - 1)n(n + 1)}{3}
$$

Now, for the inductive step we have

$$
    \begin{align*}
        \sum_{i = 1}^n i(i + 1) &= \left[ \sum_{i = 1}^{n - 1} i(i + 1) \right] + n(n + 1) \\
        &= \frac{(n - 1)n(n + 1)}{3} + \frac{3n(n + 1)}{3} \text{ (IH)} \\ \\
        &= \frac{n(n + 1)(n + 2)}{3}
    \end{align*}
$$

$$\qed$$