---
layout: post
title: Exercise 3.17 (page 57)
category: solutions-manual
displayed: false
---

## Solution:

We will construct $f(n), g(n)$ such that $f(n) > g(n)$ for $n \equiv 0 \pmod{5}$ and $g(n) \geq f(n)$ for all other $n$. To do so, we will define each function recursively.

$$
    f(n) = \begin{cases}
        f(n - 1) + g(n - 1) + 1, & \text{if $n \equiv 0 \pmod{5}$}\\
        f(n - 1) + 1, & \text{if $n \not\equiv 0 \pmod{5}$}
    \end{cases}
$$

$$
    g(n) = \begin{cases}
        g(n - 1) + 1, & \text{if $n \equiv 0 \pmod{5}$}\\
        g(n - 1) + f(n - 1) + 1, & \text{if $n \not\equiv 0 \pmod{5}$}
    \end{cases} 
$$

The initial conditions are $f(0) = 1$ and $g(0) = 0$. Now, observe that $f(n) \ne O(g(n))$ because $f(n) \not\leq cg(n)$ for all $n \equiv 0 \pmod{5}$ regardless of what $c$ is. This is due to the fact that when $n$ is a multiple of $5$, 

$$f(n) = f(n - 1) + cg(n - 1) + 1 > cg(n - 1) + 1 = g(n)$$

The same argument can be applied for $n \not\equiv 0 \pmod{5}$ to show that $g(n) \ne O(f(n))$.

$$\qed$$