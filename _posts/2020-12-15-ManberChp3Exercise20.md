---
layout: post
title: Exercise 3.20 (page 58)
category: solutions-manual
displayed: false
---

## Solution:

Assume $T\left(n - c\left(\frac{n}{c}\right)\right) = q$, where $q$ is a constant. Now,

$$
    \begin{align*}
        T(n) &= 2T(n - c) + k \\\\
        &= 2[2T(n - 2c) + k] + k \\\\
        &= 2[2[2T(n - 3c) + k] + k] + k \\\\
        &\vdots \\\\
        &= \left(2^{\frac{n}{c}}\right)T\left(n - c\left(\frac{n}{c}\right) \right) + \left(2^{\frac{n}{c} - 1}\right)k + \left(2^{\frac{n}{c} - 2}\right)k + \cdots + 2k + k \\\\
        &= \left(2^{\frac{n}{c}}\right)q + k\left(\sum_{i = 0}^{\frac{n}{c} - 1} 2^i \right) \\\\
        &= \left(2^{\frac{n}{c}}\right)q + k\left(2^{\frac{n}{c}} - 1\right) \\\\
        &= \left(2^{\frac{n}{c}}\right)(q + k) - k \\\\
        &= \left(2^{\frac{1}{c}}\right)^n(q + k) - k \\\\
        &= O\left(\left(2^{\frac{1}{c}}\right)^n\right) \\
    \end{align*}
$$

Since $d = 2^{\frac{1}{c}}$ is a constant, we are done. 

$$\qed$$