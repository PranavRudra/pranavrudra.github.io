---
layout: post
title: Exercise 3.23 (page 58)
category: solutions-manual
displayed: false
---

## Solution:

Assuming $n = 2^q$ for some $q \geq 1$, we have

$$
    \begin{align*}
        T(n) &= k\left[ T\left(\frac{n}{2^1} \right) \right] + f(n) \\\\
        &= k\left[k\left[ T\left(\frac{n}{2^2} \right) \right] + f\left(\frac{n}{2^1}\right) \right] + f(n) \\\\
        &= k\left[k\left[k\left[ T\left(\frac{n}{2^3} \right) \right] + f\left(\frac{n}{2^2}\right) \right] + f\left(\frac{n}{2^1}\right)  \right] + f(n) \\
        &\vdots \\
        &= k^q\left[ T\left(\frac{n}{2^q} \right) \right] + k^{q - 1}f\left(\frac{n}{2^{q - 1}}\right) + k^{q - 2}f\left(\frac{n}{2^{q - 2}}\right) + \cdots + kf\left(\frac{n}{2^1}\right) + f(n) \\\\
        &= k^q\left[ T\left(\frac{n}{2^q} \right) \right] + k^{q - 1}f\left(2^1 \right) + k^{q - 2}f\left(2^2\right) + \cdots + kf\left(2^{q - 1}\right) + f\left(2^q\right) \\\\
        &= k^{\log_2(n)}(c) + k^{\log_2(n) - 1}f\left(2^1 \right) + k^{\log_2(n) - 2}f\left(2^2\right) + \cdots + k^{\log_2(n) - \left(\log_2(n) - 1\right)}f\left(2^{\log_2(n) - 1}\right) + k^{\log_2(n) - \log_2(n)}f\left(2^{\log_2(n)}\right) \\\\
        &= k^{\log_2(n)}(c) + k^{\log_2(n)}\left[\frac{f\left(2^1 \right)}{k^1}\right] + k^{\log_2(n)}\left[\frac{f\left(2^2 \right)}{k^2}\right] + \cdots + k^{\log_2(n)}\left[\frac{f\left(2^{\log_2(n) - 1} \right)}{k^{\log_2(n) - 1}}\right] + k^{\log_2(n)}\left[\frac{f\left(2^{\log_2(n)} \right)}{k^{\log_2(n)}}\right] \\\\
        &= k^{\log_2(n)}\left( c + \left[\frac{f\left(2^1 \right)}{k^1}\right] + \left[\frac{f\left(2^2 \right)}{k^2}\right] + \cdots + \left[\frac{f\left(2^{\log_2(n) - 1} \right)}{k^{\log_2(n) - 1}}\right] + \left[\frac{f\left(2^{\log_2(n)} \right)}{k^{\log_2(n)}}\right] \right) \\\\
        &= n^{\log_2(k)}\left( c + \left[\frac{f\left(2^1 \right)}{k^1}\right] + \left[\frac{f\left(2^2 \right)}{k^2}\right] + \cdots + \left[\frac{f\left(2^{\log_2(n) - 1} \right)}{k^{\log_2(n) - 1}}\right] + \left[\frac{f\left(2^{\log_2(n)} \right)}{k^{\log_2(n)}}\right] \right) \\\\
        &= n^{\log_2(k)}\left( c + \left[\frac{f\left(2^1 \right)}{k^{\log_2\left(2^1 \right)}}\right] + \left[\frac{f\left(2^2 \right)}{k^{\log_2\left(2^2 \right)}}\right] + \cdots + \left[\frac{f\left(2^{\log_2(n) - 1} \right)}{k^{\log_2\left(2^{\log_2(n) - 1} \right)}}\right] + \left[\frac{f\left(2^{\log_2(n)} \right)}{k^{\log_2\left(2^{\log_2(n)} \right)}}\right] \right) \\\\
        &= n^{\log_2(k)}\left( c + \left[\frac{f\left(2^1 \right)}{\left(2^1\right)^{\log_2(k)}}\right] + \left[\frac{f\left(2^2 \right)}{\left(2^2\right)^{\log_2(k)}}\right] + \cdots + \left[\frac{f\left(2^{\log_2(n) - 1} \right)}{\left(2^{\log_2(n) - 1} \right)^{\log_2(k)}}\right] + \left[\frac{f\left(2^{\log_2(n)} \right)}{\left(2^{\log_2(n)}\right)^{\log_2(k)}}\right] \right) \\\\
        &= n^{\log_2(k)}\left( c + g(2) + g(4) + \cdots + g(n) \right) \\\\
    \end{align*}
$$

$$\qed$$