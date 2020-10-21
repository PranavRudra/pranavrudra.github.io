---
layout: post
title: Exercise 2.06 (page 31)
category: solutions-manual
displayed: false
---

## Solution:

We will induct on $k$. For the base case, consider $k = 1$. 

$$
    1^2 = (-1)^{1 - 1}\left[\frac{1(1 + 1)}{2}\right] = 1
$$

For the inductive hypothesis (IH), assume

$$
    \sum_{i = 1}^{k - 1} (-1)^{i - 1}i^2 = (-1)^{k - 2}\left[\frac{(k - 1)k}{2} \right]
$$

Now, for the inductive step we have

$$
    \begin{align*}
        \sum_{i = 1}^k (-1)^{i - 1}i^2 &= \left[ \sum_{i = 1}^{k - 1} (-1)^{i - 1}i^2 \right] + (-1)^{k - 1}k^2 \\
        &= (-1)^{k - 2}\left[\frac{(k - 1)k}{2} \right] + (-1)^{k - 1}k^2 \text{ (IH)} \\
        &= (-1)^{k - 2}\left[\frac{k(k - 1)}{2} + (-1)\frac{(2k)k}{2} \right] \\
        &= (-1)^{k - 2}\left(\frac{k}{2}\right)\left[(k - 1) - 2k \right] \\
        &= (-1)^{k - 1}\left[\frac{k(k + 1)}{2}\right]
    \end{align*}
$$

$$\qed$$