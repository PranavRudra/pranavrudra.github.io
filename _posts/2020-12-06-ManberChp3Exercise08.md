---
layout: post
title: Exercise 3.08 (page 56)
category: solutions-manual
displayed: false
---

## Solution:

We will prove that $T(n) \leq 2^{100}n(\log_2(n))^2$ for all $n \geq 2$.

For the base case, consider $n = 2$. We have 

$$T(2) = 4 \leq 2^{100}(2)(\log_2(2))^2 = 2^{101}$$

For the inductive hypothesis (IH), assume that for all $k < n$

$$T(k) \leq 2^{100}k(\log_2(k))^2$$

Now, for the inductive step, we must show that the same holds for $n$. That is,

$$
    \begin{alignat*}{2}
        T(n) &= 2T\left( \left \lfloor \frac{n}{2} \right\rfloor \right) + 2n\log_2(n) &&\text{ (by definition of $T(n)$) } \\
        &\leq 2\left[ 2^{100}\left( \left \lfloor \frac{n}{2} \right\rfloor \right) \left(\log_2\left( \left \lfloor \frac{n}{2} \right\rfloor \right) \right)^2 \right] + 2n\log_2(n) &&\text{ (by IH) } \\
        &\leq 2^{101}\left(\frac{n}{2}\right) \left(\log_2\left(\frac{n}{2}\right)\right)^2 + 2n\log_2(n) \\
        &= 2^{100} n \left(\log_2(n) - 1\right)^2 + 2n\log_2(n) \\
        &= 2^{100} n [(\log_2(n))^2 - 2\log_2(n) + 1] + 2n\log_2(n) \\
        &= 2^{100}n(\log_2(n))^2 - 2^{101}n\log_2(n) + 2^{100}n + 2n\log_2(n) \\
        &= 2^{100}n(\log_2(n))^2 + 2n[\log_2(n) + 2^{99} - 2^{100}\log_2(n)] \\
        &= 2^{100}n(\log_2(n))^2 + 2n[2^{99} + (1 - 2^{100})\log_2(n)] \\
        &\leq 2^{100}n(\log_2(n))^2
    \end{alignat*}
$$

This completes the proof. Thus, since $2^{100}$ is a constant, $T(n) = O(n(\log_2(n))^2)$.

$$\qed$$