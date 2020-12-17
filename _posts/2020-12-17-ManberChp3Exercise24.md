---
layout: post
title: Exercise 3.24 (page 59)
category: solutions-manual
displayed: false
---

## Solution:

Assuming $n = d^q$ for some $q \geq 1$, we have

$$
    \begin{align*}
        T(n) &= k\left[ T\left(\frac{n}{d^1} \right) \right] + f(n) \\\\
        &= k\left[k\left[ T\left(\frac{n}{d^2} \right) \right] + f\left(\frac{n}{d^1}\right) \right] + f(n) \\\\
        &= k\left[k\left[k\left[ T\left(\frac{n}{d^3} \right) \right] + f\left(\frac{n}{d^2}\right) \right] + f\left(\frac{n}{d^1}\right)  \right] + f(n) \\
        &\vdots \\
        &= k^q\left[ T\left(\frac{n}{d^q} \right) \right] + k^{q - 1}f\left(\frac{n}{d^{q - 1}}\right) + k^{q - 2}f\left(\frac{n}{d^{q - 2}}\right) + \cdots + kf\left(\frac{n}{d^1}\right) + f(n) \\\\
        &= k^q\left[ T\left(\frac{n}{d^q} \right) \right] + k^{q - 1}f\left(d^1 \right) + k^{q - 2}f\left(d^2\right) + \cdots + kf\left(d^{q - 1}\right) + f\left(d^q\right) \\\\
        &= k^{\log_d(n)}(c) + k^{\log_d(n) - 1}f\left(d^1 \right) + k^{\log_d(n) - 2}f\left(d^2\right) + \cdots + k^{\log_d(n) - \left(\log_d(n) - 1\right)}f\left(d^{\log_d(n) - 1}\right) + k^{\log_d(n) - \log_d(n)}f\left(d^{\log_d(n)}\right) \\\\
        &= k^{\log_d(n)}(c) + k^{\log_d(n)}\left[\frac{f\left(d^1 \right)}{k^1}\right] + k^{\log_d(n)}\left[\frac{f\left(d^2 \right)}{k^2}\right] + \cdots + k^{\log_d(n)}\left[\frac{f\left(d^{\log_d(n) - 1} \right)}{k^{\log_d(n) - 1}}\right] + k^{\log_d(n)}\left[\frac{f\left(d^{\log_d(n)} \right)}{k^{\log_d(n)}}\right] \\\\
        &= k^{\log_d(n)}\left( c + \left[\frac{f\left(d^1 \right)}{k^1}\right] + \left[\frac{f\left(d^2 \right)}{k^2}\right] + \cdots + \left[\frac{f\left(d^{\log_d(n) - 1} \right)}{k^{\log_d(n) - 1}}\right] + \left[\frac{f\left(d^{\log_d(n)} \right)}{k^{\log_d(n)}}\right] \right) \\\\
        &= n^{\log_d(k)}\left( c + \left[\frac{f\left(d^1 \right)}{k^1}\right] + \left[\frac{f\left(d^2 \right)}{k^2}\right] + \cdots + \left[\frac{f\left(d^{\log_d(n) - 1} \right)}{k^{\log_d(n) - 1}}\right] + \left[\frac{f\left(d^{\log_d(n)} \right)}{k^{\log_d(n)}}\right] \right) \\\\
        &= n^{\log_d(k)}\left( c + \left[\frac{f\left(d^1 \right)}{k^{\log_d\left(d^1 \right)}}\right] + \left[\frac{f\left(d^2 \right)}{k^{\log_d\left(d^2 \right)}}\right] + \cdots + \left[\frac{f\left(d^{\log_d(n) - 1} \right)}{k^{\log_d\left(d^{\log_d(n) - 1} \right)}}\right] + \left[\frac{f\left(d^{\log_d(n)} \right)}{k^{\log_d\left(d^{\log_d(n)} \right)}}\right] \right) \\\\
        &= n^{\log_d(k)}\left( c + \left[\frac{f\left(d^1 \right)}{\left(d^1\right)^{\log_d(k)}}\right] + \left[\frac{f\left(d^2 \right)}{\left(d^2\right)^{\log_d(k)}}\right] + \cdots + \left[\frac{f\left(d^{\log_d(n) - 1} \right)}{\left(d^{\log_d(n) - 1} \right)^{\log_d(k)}}\right] + \left[\frac{f\left(d^{\log_d(n)} \right)}{\left(d^{\log_d(n)}\right)^{\log_d(k)}}\right] \right) \\\\
        &= n^{\log_d(k)}\left( c + g(d) + g(d^2) + \cdots + g(n) \right) \\\\
    \end{align*}
$$

$$\qed$$