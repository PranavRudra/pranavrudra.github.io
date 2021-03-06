---
layout: post
title: Exercise 2.14 (page 32)
category: solutions-manual
displayed: false
---

## Solution:

We will induct on $n$, the positive integer we are writing as a sum. For the base cases, consider

$$
    \begin{align*}
        1 &= 1 \\
        2 &= 2 \\
        3 &= 3 \\
        4 &= 4 \\
        5 &= 5 \\
        6 &= 5 + 1 \\
        7 &= 5 + 2 \\
        8 &= 5 + 3 \\
        9 &= 5 + 4
    \end{align*}
$$

For the inductive hypothesis (IH), assume that for $10 \leq k < n$ we can write $k$ as a sum of distinct elements of the sequence. Now, for the inductive step, we will show that we can do the same for $n$. Let $t$ be the largest element of the sequence that is less than $n$ and $a_i = 10(2^{i - 1})$ denote the $i$-th element of the geometric part of the sequence. Hence, we have $t = a_q$ where

$$
    q = \left\lfloor \log_2\left(\frac{n}{10}\right) \right\rfloor + 1 = \left\lfloor \log_2(n) - 3 \right\rfloor + 1
$$

We now have two cases. If $n - t = 0$, then $n = t$ is a sum of distinct elements of the sequence as desired. However, if $n - t > 0$, we claim that we can write $n - t$ as a sum of distinct elements of the sequence by the induction hypothesis. Further, we claim that adding $t$ to this sum (to give a sum representation of $n$) will not duplicate any existing elements. That is, $n - t$ does not contain $t$ in its sum. 

Since $n \geq 10$ by IH, $q \geq 1$ and $t = a_q \geq 10$. Therefore, $n - t \leq n - 10 < n$. This allows us to invoke the induction hypothesis to claim that $n - t$ can be written as a sum of distinct elements of the sequence. Now, suppose for the sake of contradiction that $n - t$ contains $t$ in its sum. Then, $n \geq 2t$, which implies that $t$ is not the largest element of the sequence that is less than $n$ ($a_{q + 1} = 2a_q = 2t \leq n$ is larger still). This contradicts the choice of $t$.

Thus, $n - t$ can be written as a sum of distinct elements of the sequence, each of which is strictly less than $t$. Hence, adding $t$ to this sum gives a sum representation of $n$ where each of the elements are distinct. This completes the proof.

$$\qed$$