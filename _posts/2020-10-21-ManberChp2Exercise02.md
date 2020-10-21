---
layout: post
title: Exercise 2.02 (page 31)
category: solutions-manual
displayed: false
---

## Solution:

We will use induction. First, we conjecture that

$$
    \begin{align*}
        \sum_{i = 1}^{n} a_i &= [c_1(1) + c_2] + [c_1(2) + c_2] + \cdots + [c_1(n) + c_2] \\
        &= c_1(1 + 2 + \cdots + n) + nc_2 \\
        &= c_1\left(\frac{n(n + 1)}{2}\right) + \frac{2nc_2}{2} \\
        &= \left(\frac{n}{2}\right)[c_1(n + 1) + 2c_2]
    \end{align*}    
$$

For the base case, consider $n = 1$. Clearly, 

$$
     a_1 = \left(\frac{1}{2}\right)(2c_1 + 2c_2) = c_1(1) + c_2
$$ 

For the inductive hypothesis (IH), assume

$$
    \sum_{i = 1}^{n - 1} a_i = \left(\frac{n - 1}{2}\right)[c_1n + 2c_2]
$$

Now, for the inductive step we have

$$
    \begin{align*}
        \sum_{i = 1}^n a_i &= \left(\sum_{i = 1}^{n - 1} a_i\right) + a_n \\
        &= \left(\frac{n - 1}{2}\right)[c_1n + 2c_2] + [c_1n + c_2] \text{ (IH)} \\
        &= c_1\left(\frac{n(n + 1)}{2}\right) + nc_2 \\
        &= \left(\frac{n}{2}\right)[c_1(n + 1) + 2c_2]
    \end{align*}
$$

$$\qed$$