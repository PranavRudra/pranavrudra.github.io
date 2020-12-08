---
layout: post
title: Exercise 3.16 (page 57)
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
    \frac{f(n)}{g(n)} = \frac{n}{(\log_2(n))^2} = O(n) \ne O\left(\frac{n}{n} \right)
$$

since $\frac{n}{(\log_2(n))^2} \leq cn$ for all $n \geq 2$ and $c \geq 1$.

$$\qed$$