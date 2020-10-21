---
layout: post
title: Exercise 2.08 (page 31)
category: solutions-manual
displayed: false
---

## Solution:

We will induct on $n$. For the base case, consider $n = 1$.

$$
    2^{1 - 1}(a^1 + b^1) = (a + b) \geq (a + b) = (a + b)^1
$$

For the inductive hypothesis (IH), assume

$$
    2^{n - 2}(a^{n - 1} + b^{n - 1}) \geq (a + b)^{n - 1}
$$

Now, for the inductive step we have

$$
    \begin{align*}
        (a + b)^n &= (a + b)^{n - 1}(a + b) \\
        &\leq 2^{n - 2}(a^{n - 1} + b^{n - 1})(a + b) \text{ (IH)} \\
        &= 2^{n - 2}(a^n + b^n + ab^{n - 1} + ba^{n - 1}) \\
        &\leq 2^{n - 2}(a^n + b^n) \\
        &\leq 2^{n - 1}(a^n + b^n)
    \end{align*}
$$

$$\qed$$