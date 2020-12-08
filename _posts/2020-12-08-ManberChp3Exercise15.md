---
layout: post
title: Exercise 3.15 (page 57)
category: solutions-manual
displayed: false
---

## Solution:

Consider $f(n) = n$ and $g(n) = (\log_2(n))^2$. 

By theorem $3.1$, we have 

$$
    g(n) = O(2^{\log_2(n)}) = O(n)
$$ 

Also, clearly 

$$
    f(n) = O(n)
$$

Hence, $s(n) = r(n) = n$. However, 

$$
    f(n) - g(n) = n - (\log_2(n))^2 = O(n) \ne O(n - n)
$$

since $n - (\log_2(n))^2 \leq cn$ for all $n \geq 1$ and $c \geq 1$.

$$\qed$$