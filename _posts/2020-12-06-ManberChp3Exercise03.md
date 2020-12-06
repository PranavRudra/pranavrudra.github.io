---
layout: post
title: Exercise 3.03 (page 56)
category: solutions-manual
displayed: false
---

## Solution:

NOTE: The text has a printing error. The problem should say $n^{\frac{1}{5}}(\log_3(n))^5 = O(n^{1.2})$

Clearly, $n^{\frac{1}{5}} = O(n^{\frac{1}{5}})$. Also, by theorem $3.1$, we have

$$(\log_3(n))^5 = O(3^{\log_3(n)}) = O(n)$$

Therefore, by lemma $3.2$, 

$$n^{\frac{1}{5}}(\log_3(n))^5 = O(n^{\frac{1}{5}}n) = O(n^{1.2})$$