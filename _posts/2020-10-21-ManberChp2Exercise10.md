---
layout: post
title: Exercise 2.10 (page 31)
category: solutions-manual
displayed: false
---

## Solution:

Let $a_{i,j}$ be the $j$-th entry in the $i$-th row of the Pascal triangle. Then we can define 

$$
    a_{i, j} = \begin{cases} 
        1 &\mbox{if } i = 1, j = 1 \\
        0 &\mbox{if } j = 0 \\
        0 &\mbox{if } j > i \\
        a_{i - 1, j - 1} + a_{i - 1, j} &\mbox{otherwise}
    \end{cases}
$$

We will prove that 

$$
    \sum_{j = 1}^n a_{n, j} = 2^{n - 1}
$$ 

by induction on $n$. For the base case, consider $n = 1$. Clearly,

$$
    \sum_{j = 1}^1 a_{1, j} = a_{1, 1} = 1 = 2^{1 - 1}
$$

For the induction hypothesis (IH), assume the claim holds for $n - 1$. Now,

$$
    \begin{align*}
        \sum_{j = 1}^n a_{n, j} &= \sum_{j = 1}^n (a_{n - 1, j - 1} + a_{n - 1, j}) \\
        &= \sum_{j = 1}^n a_{n - 1, j - 1} + \sum_{j = 1}^n a_{n - 1, j} \\
        &= \sum_{j = 2}^n a_{n - 1, j - 1} + \sum_{j = 1}^{n - 1} a_{n - 1, j} \text{ ($a_{n - 1, 0} = a_{n - 1, n} = 0$)} \\
        &= \sum_{j = 1}^{n - 1} a_{n - 1, j} + \sum_{j = 1}^{n - 1} a_{n - 1, j} \\
        &= 2(2^{n - 2}) = 2^{n - 1} \text{ (IH)}
    \end{align*}
$$

$$\qed$$