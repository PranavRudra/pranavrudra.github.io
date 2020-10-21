---
layout: post
title: Exercise 2.11 (page 32)
category: solutions-manual
displayed: false
---

## Solution:

Let $a_{i,j}$ be the $j$-th entry in the $i$-th row of the triangle. Then we can define 

$$
    a_{i, j} = \begin{cases} 
        1 &\mbox{if } i = 1, j = 1 \\
        0 &\mbox{if } j \leq 0 \\
        0 &\mbox{if } j > 2i - 1 \\
        a_{i - 1, j - 2} + a_{i - 1, j - 1} + a_{i - 1, j} &\mbox{otherwise}
    \end{cases}
$$

We will prove that 

$$
    \sum_{j = 1}^{2n - 1} a_{n, j} = 3^{n - 1}
$$ 

by induction on $n$. For the base case, consider $n = 1$. Clearly,

$$
    \sum_{j = 1}^{2(1) - 1} a_{1, j} = a_{1, 1} = 1 = 3^{1 - 1}
$$

For the induction hypothesis (IH), assume the claim holds for $n - 1$. Now,

$$
    \begin{align*}
        \sum_{j = 1}^{2n - 1} a_{n, j} &= \sum_{j = 1}^{2n - 1} (a_{n - 1, j - 2} + a_{n - 1, j - 1} + a_{n - 1, j}) \\
        &= \sum_{j = 1}^{2n - 1} a_{n - 1, j - 2} + \sum_{j = 1}^{2n - 1} a_{n - 1, j - 1} + \sum_{j = 1}^{2n - 1} a_{n - 1, j} \\
        &= \sum_{j = 3}^{2n - 1} a_{n - 1, j - 2} + \sum_{j = 2}^{2n - 2} a_{n - 1, j - 1} + \sum_{j = 1}^{2n - 3} a_{n - 1, j} \\
        &= \sum_{j = 1}^{2n - 3} a_{n - 1, j} + \sum_{j = 1}^{2n - 3} a_{n - 1, j} + \sum_{j = 1}^{2n - 3} a_{n - 1, j} \\
        &= 3(3^{n - 2}) = 3^{n - 1} \text{ (IH)}
    \end{align*}
$$

$$\qed$$