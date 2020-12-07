---
layout: post
title: Exercise 3.07 (page 56)
category: solutions-manual
displayed: false
---

## Solution:

Since this recurrence looks similar to the Fibonacci recurrence we will try $T(n) = c(a^n)$.

$$
    \begin{align*}
        T(n) &= 8T(n - 1) - 15T(n - 2) \\
        ca^n &= 8ca^{n - 1} - 15ca^{n - 2} \\
        a^2 &= 8a - 15 \\
        a &= 3, 5
    \end{align*}
$$

Now, given that any linear combination of these roots solves the recurrence, we have

$$
    \begin{alignat*}{3}
        T(1) &= 1 &&= c_1(3) &&+ c_2(5) \\
        T(2) &= 4 &&= c_1(3^2) &&+ c_2(5^2) \\
    \end{alignat*}
$$

Solving for the constants yields $c_1 = \frac{1}{6}$, $c_2 = \frac{1}{10}$. Thus, we can write

$$
    T(n) = \frac{1}{6}3^n + \frac{1}{10}5^n 
$$