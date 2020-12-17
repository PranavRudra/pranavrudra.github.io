---
layout: post
title: Exercise 3.22 (page 58)
category: solutions-manual
displayed: false
---

## Solution:

a)

$$
    \begin{align*}
        T(n) &= 4T\left(n^{(\frac{1}{2})^1}\right) + 1 \\\\
        &= 4\left[4T\left(n^{(\frac{1}{2})^2}\right) + 1  \right] + 1 \\\\
        &= 4\left[4\left[4T\left(n^{(\frac{1}{2})^3}\right) + 1  \right] + 1 \right] + 1 \\
        &\vdots \\
        &= 4^xT\left(n^{(\frac{1}{2})^x}\right) + 4^{x - 1}(1) + 4^{x - 2}(1) + \cdots + 4(1) + 1 \\\\
        &= 4^xT\left(n^{(\frac{1}{2})^x}\right) + \sum_{i = 0}^{x - 1} 4^i \\\\
        &= 4^xT\left(n^{(\frac{1}{2})^x}\right) + \frac{4^x - 1}{4 - 1}
    \end{align*}
$$

In order for $T\left(n^{(\frac{1}{2})^x}\right)$ to be the base case, we must find $x$ such that $n^{(\frac{1}{2})^x} = 2$

$$
    \begin{align*}
        n^{(\frac{1}{2})^x} &= 2 \\\\
        \left(\frac{1}{2}\right)^x \log_2(n) &= 1 \\\\
        \left(\frac{1}{2}\right)^x &= \frac{1}{\log_2(n)} \\\\
        x(-1) &= \log_2\left(\frac{1}{\log_2(n)} \right) \\\\
        x(-1) &= \log_2(1) - \log_2\left(\log_2(n) \right) \\\\
        x &= \log_2\left(\log_2(n) \right)
    \end{align*}
$$

Now, we have

$$
    \begin{align*}
        T(n) &= 4^{\log_2\left(\log_2(n) \right)}T(2) + \frac{4^{\log_2\left(\log_2(n) \right)} - 1}{3} \\\\
        &= \frac{3\left(4^{\log_2\left(\log_2(n) \right)} \right)}{3} + \frac{4^{\log_2\left(\log_2(n) \right)} - 1}{3} \\\\
        &= \frac{4\left(4^{\log_2\left(\log_2(n) \right)} \right) - 1}{3} \\\\
        &= \frac{4\left(2^{2\log_2\left(\log_2(n) \right)} \right) - 1}{3} \\\\
        &= \frac{4\left(2^{\log_2\left(\left(\log_2(n)\right)^2 \right)} \right) - 1}{3} \\\\
        &= \frac{4\left(\left(\log_2(n)\right)^2 \right) - 1}{3} \\\\
        &= O\left(\left(\log(n)\right)^2 \right)
    \end{align*}
$$

b)

$$
    \begin{align*}
        T(n) &= 2T\left(n^{(\frac{1}{2})^1}\right) + 2n \\\\
        &= 2\left[2T\left(n^{(\frac{1}{2})^2}\right) + 2n  \right] + 2n \\\\
        &= 2\left[2\left[2T\left(n^{(\frac{1}{2})^3}\right) + 2n  \right] + 2n \right] + 2n \\
        &\vdots \\
        &= 2^xT\left(n^{(\frac{1}{2})^x}\right) + 2^{x - 1}(2n) + 2^{x - 2}(2n) + \cdots + 2(2n) + 2n \\\\
        &= 2^xT\left(n^{(\frac{1}{2})^x}\right) + \sum_{i = 0}^{x - 1} (2n)^i \\\\
        &= 2^xT\left(n^{(\frac{1}{2})^x}\right) + \frac{(2n)^x - 1}{2n - 1}
    \end{align*}
$$

where $x = \log_2\left(\log_2(n)\right)$. 

$$
    \begin{align*}
        T(n) &= 2^{\log_2\left(\log_2(n)\right)}T(2) + \frac{(2n)^{\log_2\left(\log_2(n)\right)} - 1}{2n - 1} \\\\
        &= \log_2(n) +  \frac{\left(\log_2(n)\right)n^{\log_2\left(\log_2(n)\right)} - 1}{2n - 1} \\\\
        &= \log_2(n) + \frac{\left(\log_2(n)\right)^{\log_2(n) + 1} - 1}{2n - 1} \\\\
        &= \log_2(n) + \frac{\left(\log_2(n)\right)^{\log_2(n) + 1} - 1}{2\left(2^{\log_2(n)}\right) - 1} \\\\
        &= \log_2(n) + \frac{\left(\log_2(n)\right)^{\log_2(n) + 1} - 1}{2^{\log_2(n) + 1} - 1} \\\\
        &\leq C\left(\frac{\log_2(n)}{2}\right)^{\log_2(n) + 1} \\\\
        &\leq C\left(\log_2(n)\right)^{\log_2(n) + 1}
    \end{align*}
$$

where $C$ is a large constant. Thus,

$$
    \begin{align*}
        T(n) &= O\left(\log(n)^{\log(n)} \right)
    \end{align*}
$$

$$\qed$$