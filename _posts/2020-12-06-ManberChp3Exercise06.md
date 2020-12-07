---
layout: post
title: Exercise 3.06 (page 56)
category: solutions-manual
displayed: false
---

## Solution:

We expand the recurrence to get a feel for it.

$$
    \begin{align*}
        T(n) &= T(n - 1) + \frac{n}{2} \\ \\ 
        T(n - 1) &= T(n - 2) + \frac{(n - 1)}{2} \\ \\
        T(n - 2) &= T(n - 3) + \frac{(n - 2)}{2} \\ \\
        &\vdots \\
        T(3) &= T(2) + \frac{3}{2} \\ \\ 
        T(2) &= T(1) + \frac{2}{2} \\ \\
        T(1) &= 1
    \end{align*}
$$

Hence, we propose that

$$T(n) = 1 + \sum_{i = 2}^{n} \frac{i}{2} = 1 + \left(\frac{1}{2}\right)\left(\frac{n - 1}{2}\right)(n + 2) = \frac{(n - 1)(n + 2) + 4}{4}$$

We can now prove this via induction on $n$. For the base case, consider $n = 1$. Clearly, 

$$T(1) = \frac{(1 - 1)(1 + 2) + 4}{4} = \frac{4}{4} = 1$$

For the inductive hypothesis (IH), assume that

$$T(n - 1) = \frac{(n - 2)(n + 1) + 4}{4}$$

Now, for the inductive step, we have

$$
    \begin{alignat*}{2}
        T(n) &= T(n - 1) + \frac{n}{2} &&\text{ (by definition of $T(n)$) } \\ \\
        &= \frac{(n - 2)(n + 1) + 4}{4} + \frac{n}{2}  &&\text{ (by IH) } \\ \\
        &= \frac{n^2 + n + 2}{4} \\ \\
        &= \frac{n^2 + n - 2 + 4}{4} \\ \\
        &= \frac{(n - 1)(n + 2) + 4}{4}
    \end{alignat*}
$$

$$\qed$$