---
layout: post
title: Exercise 3.26 (page 59)
category: solutions-manual
displayed: false
---

## Solution:

This is a divide-and-conquer recurrence with $a = 1, b = 2, c = \frac{1}{2}$. Since

$$
    a = 1 < \sqrt{2} = 2^{\frac{1}{2}} = b^k
$$

we apply the third case of the master theorem. Hence, 

$$T(n) = O\left(n^{\frac{1}{2}}\right) = O(\sqrt{n})$$

$$\qed$$