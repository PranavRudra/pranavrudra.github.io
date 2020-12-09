---
layout: post
title: Exercise 3.18 (page 58)
category: solutions-manual
displayed: false
---

## Solution:

We solve the recurrence for a few values of $n$ to get a feel for it.

$$
    \begin{align*}
        T(2) &= 1 \\
        T(4) &= 2T(2) + 1 = 3 \\
        T(8) &= 2T(4) + 1 = 7 \\
        T(16) &= 2T(8) + 1 = 15
    \end{align*}
$$

Hence, we propose that $T(n) = n - 1$. We can prove this via induction.

For the base case, consider $n = 2$. 

$$
    T(2) = 2 - 1 = 1
$$

For the inductive hypothesis (IH), assume $\forall k < n$

$$
    T(k) = k - 1
$$

Now, for the inductive step, we must show the claim holds for $n$.

$$
    \begin{alignat*}{2}
        T(n) &= 2T\left(\frac{n}{2}\right) + 1 &&\text{ (by definition of $T(n)$)} \\
        &= 2\left(\frac{n}{2} - 1\right) + 1 &&\text{ (by IH)} \\
        &= n - 1
    \end{alignat*}
$$

$$\qed$$