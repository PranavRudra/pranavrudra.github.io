---
layout: post
title: Exercise 3.09 (page 56)
category: solutions-manual
displayed: false
---

## Solution:

This is a divide-and-conquer recurrence relation so we can apply the master theorem. Note that $a = 143640, b = 70, k = 2$. Since $143640 > 70^2 = 4900$, we apply the first case. Hence, the asymptotic running time of this algorithm is given by $O(n^{\log_{70}(143640)})$, or roughly $O(n^{2.795})$.

$$\qed$$