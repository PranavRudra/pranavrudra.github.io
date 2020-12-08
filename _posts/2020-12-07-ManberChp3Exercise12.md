---
layout: post
title: Exercise 3.12 (page 57)
category: solutions-manual
displayed: false
---

## Solution:

We apply the shifting technique to eliminate the history of the recurrence relation. Since

$$
    T(n + 1) - T(n) = \left[ (n + 1) + \sum_{i = 1}^{n}T(i) \right] - \left[ n + \sum_{i = 1}^{n - 1}T(i) \right] = 1 + T(n)
$$

we have

$$
    T(n + 1) = 1 + 2T(n);\ T(1) = 1
$$

We now solve the recurrence for a few values of $n$ to get a feel for it.

$$
    \begin{align*}
        T(1) &= 1 \\
        T(2) &= 1 + 2(1) = 3 \\
        T(3) &= 1 + 2(3) = 7 \\
        T(4) &= 1 + 2(7) = 15
    \end{align*}
$$

Hence, we propose that $T(n) = 2^n - 1$. We can now prove this via induction on $n$.

For the base case, consider $n = 1$

$$
    T(1) = 2^1 - 1 = 1
$$

For the inductive hypothesis (IH), assume that for all $k < n$

$$
    T(k) = 2^k - 1
$$

Now, for the inductive step, we must show that the claim holds for $n$.

$$
    \begin{alignat*}{2}
        T(n) &= 1 + 2T(n - 1) &&\text{ (by the definition of $T(n)$)} \\
        &= 1 + 2(2^{n - 1} - 1) &&\text{ (by IH)} \\
        &= 2^n - 1
    \end{alignat*}
$$

$$\qed$$