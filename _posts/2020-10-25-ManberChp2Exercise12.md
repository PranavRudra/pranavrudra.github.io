---
layout: post
title: Exercise 2.12 (page 32)
category: solutions-manual
displayed: false
---

## Solution:

We will induct on $n$. For the base case, consider $n = 2$. Clearly,

$$
    \frac{1}{3} + \frac{1}{4} = \frac{8}{24} + \frac{6}{24} = \frac{14}{24} > \frac{13}{24}
$$

For the inductive hypothesis (IH), assume

$$
    \frac{1}{n} + \frac{1}{n + 1} + \cdots + \frac{1}{2(n - 1)} > \frac{13}{24}
$$

Now, for the inductive step, observe that (lemma)

$$
    \frac{1}{2n - 1} + \frac{1}{2n} - \frac{1}{n} = \frac{2n + (2n - 1) - 2(2n - 1)}{2n(2n - 1)} = \frac{1}{2n(2n - 1)} > 0
$$

Therefore, we have

$$
    \begin{align*}
        \frac{1}{n + 1} + \frac{1}{n + 2} + \cdots + \frac{1}{2n - 1} + \frac{1}{2n} &= 
        \left[\frac{1}{n} + \frac{1}{n + 1} + \cdots + \frac{1}{2(n - 1)} \right] + \left[\frac{1}{2n - 1} + \frac{1}{2n} - \frac{1}{n} \right] \\
        &> \left[\frac{1}{n} + \frac{1}{n + 1} + \cdots + \frac{1}{2(n - 1)}\right] \text{ (lemma)} \\
        &> \frac{13}{24} \text{ (IH)}
    \end{align*}
$$

$$\qed$$