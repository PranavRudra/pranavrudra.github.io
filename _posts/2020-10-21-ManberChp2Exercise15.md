---
layout: post
title: Exercise 2.15 (page 32)
category: solutions-manual
displayed: false
---

## Solution:

NOTE: while it's true that not every positive integer can be written a sum of distinct elements of the sequence, the counterexample given in the book is wrong (i.e. $81 = 54 + 24 + 3$). A correct counterexample would be $49$. Suppose we were to copy paste our proof from the previous problem here and apply the induction principle to show that since we can form the desired sum for $1 \leq k \leq 48$, we can also do it for $49$. Given that $t = 24$ here, clearly $49 - 24 < 49$. Therefore, we can invoke the induction hypothesis to claim that $49 - 24 = 25$ can be written as a sum of distinct elements of the sequence (i.e. $25 = 24 + 1$). However, we cannot claim that $t = 24$ is not part of this sum by the same logic. 

Suppose that we try to do so anyways. Then, it's true that $n = 49 \geq 2t = 48$. However, since $24$ is the last element of the geometric part of the sequence, there is no $2(24) = 48$ that we can use for $t$ instead of $24$. As a result, $24$ must be a part of the sum representation of $25$. However, this implies that $49 = 24 + (24 + 1)$, which contains duplicate sequence elements. Thus, our proof of the previous problem does not apply to this sequence.

$$\qed$$