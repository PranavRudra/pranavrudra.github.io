---
layout: post
title: Exercise 3.19 (page 58)
category: solutions-manual
displayed: false
---

## Solution:

Assuming $n = m^k$ for some $k \geq 1$, we have

$$
    \begin{align*}
        S(n) &\leq cm\log_2(m)S\left(\frac{n}{m}\right) + O(n)\\\\
        &\leq cm\log_2(m)\left[cm\log_2(m)S\left(\frac{n}{m^2}\right) + O\left(\frac{n}{m}\right)  \right] + O(n) \\\\
        &\leq cm\log_2(m)\left[cm\log_2(m)\left[cm\log_2(m)S\left(\frac{n}{m^3}\right) + O\left(\frac{n}{m^2}\right) \right] + O\left(\frac{n}{m}\right) \right] + O(n) \\\\
        &\vdots \\\\
        &\leq (cm\log_2(m))^kS(1) + (cm\log_2(m))^{k - 1}O\left(\frac{n}{m^{k - 1}}\right) + \cdots + (cm\log_2(m))O\left(\frac{n}{m}\right) + O(n) \\\\
        &\leq (cm\log_2(m))^kS(1) + (c\log_2(m))^{k - 1}O(n) + \cdots + (c\log_2(m))O(n) + O(n) \\\\
        &\leq (cm\log_2(m))^kS(2) + O(n)\left[\sum_{i = 0}^{k - 1} (c\log_2(m))^i\right] \\\\
        &= (cm\log_2(m))^k + O(n)\left[\frac{(c\log_2(m))^k - 1}{c\log_2(m) - 1} \right] \\\\
        &= O((cm\log_2(m))^k) + O(n) \cdot O((c\log_2(m))^{k - 1}) \\\\
        &= O((cm\log_2(m))^k) + O(n(c\log_2(m))^{k - 1}) \\\\
        &= O((c\log_2(m))^{k - 1}[m^kc\log_2(m) + n]) \\\\
        &= O((c\log_2(m))^{\log_m(n) - 1}[nc\log_2(m) + n]) \\\\
        &= O\left(\frac{(c\log_2(m))^{\log_m(n)}n[c\log_2(m) + 1]}{c\log_2(m)} \right) \\\\
        &= O\left(\frac{(c^{\log_m(n)})(\log_2(m))^{\log_m(n)}n[c\log_2(m) + 1]}{c\log_2(m)} \right) \\\\
        &= O\left(\frac{n^{\log_m(c)}n^{\log_m\left(\log_2(m)\right)}n[c\log_2(m) + 1]}{c\log_2(m)} \right) \\\\
        &= O\left(n^{\log_m(c)}n^{\log_m\left(\log_2(m)\right)}n\right) \\\\
        &= O\left(n^{\log_m(c)\ +\ \log_m\left(\log_2(m)\right)\ +\ \log_m(m)} \right) \\\\
        &= O\left(n^{\log_m\left(cm \log_2(m) \right)} \right)
    \end{align*}
$$

Alternatively, we can use the master theorem with $a = cm\log_2(m)$, $b = m$, and $k = 1$. 

$$a = cm\log_2(m) > m = b^k$$

so we apply the first case. This gives us

$$T(n) = O(n^{\log_m(cm\log(m))})$$

which matches the analysis above. 

$$\qed$$