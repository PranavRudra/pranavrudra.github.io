---
layout: post
title: Exercise 2.04 (page 31)
category: solutions-manual
displayed: false
---

## Solution:

We will use induction. First, we conjecture (using some familiar formulas) that

$$
    \sum_{i = 1}^n \frac{1}{2^i} = \frac{\frac{1}{2}\left(1 - \left(\frac{1}{2}\right)^n \right)}{\frac{1}{2}} = 1 - \left(\frac{1}{2}\right)^n = \frac{2^n - 1}{2^n}
$$

For the base case, consider $n = 1$. Clearly, 

$$
   \sum_{i = 1}^1 \frac{1}{2^i} = \frac{1}{2} = \frac{2^1 - 1}{2^1}
$$ 

For the inductive hypothesis (IH), assume

$$
    \sum_{i = 1}^{n - 1} \frac{1}{2^i} = \frac{2^{n - 1} - 1}{2^{n - 1}}
$$

Now, for the inductive step we have

$$
    \begin{align*}
        \sum_{i = 1}^n \frac{1}{2^i} &= \left[ \sum_{i = 1}^{n - 1} \frac{1}{2^i} \right] + \frac{1}{2^n} \text{ (IH)} \\
        &= \frac{2^{n - 1} - 1}{2^{n - 1}} + \frac{1}{2^n} \\
        &= \frac{2^n - 2 + 1}{2^n} \\
        &= \frac{2^n - 1}{2^n}
    \end{align*}
$$

$$\qed$$