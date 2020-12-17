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
        &= 2\left[2T\left(n^{(\frac{1}{2})^2}\right) + 2\left(n^{(\frac{1}{2})^1}\right)  \right] + 2n \\\\
        &= 2\left[2\left[2T\left(n^{(\frac{1}{2})^3}\right) + 2\left(n^{(\frac{1}{2})^2}\right)  \right] + 2\left(n^{(\frac{1}{2})^1}\right) \right] + 2n \\
        &\vdots \\
        &= 2^xT\left(n^{(\frac{1}{2})^x}\right) + 2^{x - 1}(2)\left(n^{(\frac{1}{2})^{x - 1}}\right) + 2^{x - 2}(2)\left(n^{(\frac{1}{2})^{x - 2}}\right) + \cdots + 2n\\\\
        &= 2^{x - 0}T\left(n^{(\frac{1}{2})^{x - 0}}\right) + 2^{x - 0}\left(n^{(\frac{1}{2})^{x - 1}}\right) + 2^{x - 1}\left(n^{(\frac{1}{2})^{x - 2}}\right) + \cdots + 2^{x - (x - 1)}n^{(\frac{1}{2})^{x - x}}
    \end{align*}
$$

where $x = \log_2\left(\log_2(n)\right)$. Now, observe that

$$
    \begin{align*}
        2^{x - j} = 2^{\log_2\left(\log_2(n)\right) - j} = \frac{2^{\log_2\left(\log_2(n)\right)}}{2^j} = \frac{\log_2(n)}{2^j}
    \end{align*}
$$

Additionally, given that

$$
    \begin{align*}
        \left(\frac{1}{2}\right)^{x - j} = \left(\frac{1}{2}\right)^{\log_2\left(\log_2(n)\right) - j} = \frac{\left(\frac{1}{2}\right)^{\log_2\left(\log_2(n)\right)}}{\left(\frac{1}{2}\right)^j} = \frac{2^{-\log_2\left(\log_2(n)\right)}}{\frac{1}{2^j}} = \frac{2^{\log_2\left(\frac{1}{\log_2(n)}\right)}}{\frac{1}{2^j}} = \frac{\frac{1}{\log_2(n)}}{\frac{1}{2^j}} = \frac{2^j}{\log_2(n)}
    \end{align*}
$$

we can simplify

$$
    \begin{align*}
        n^{\left(\frac{1}{2}\right)^{x - j}} = n^{\frac{2^j}{\log_2(n)}} = \left(n^{\frac{1}{\log_2(n)}}\right)^{2^j} = 2^{2^j}
    \end{align*}
$$

Hence,

$$
    \begin{align*}
        T(n) &= \log_2(n)T(2) + \left(\frac{\log_2(n)}{2^0}\right)\left(2^{2^1} \right) + \left(\frac{\log_2(n)}{2^1}\right)\left(2^{2^2} \right) + \left(\frac{\log_2(n)}{2^2}\right)\left(2^{2^3} \right) + \cdots + \left(\frac{\log_2(n)}{2^{\log_2\left(\log_2(n)\right) - 1}}\right)\left(2^{2^{\log_2\left(\log_2(n)\right)}} \right) \\\\
        &= \log_2(n) + \left(\frac{\log_2(n)}{2^0}\right)\left(2^{2^1} \right) + \left(\frac{\log_2(n)}{2^1}\right)\left(2^{2^2} \right) + \left(\frac{\log_2(n)}{2^2}\right)\left(2^{2^3} \right) + \cdots + \left(\frac{\log_2(n)}{2^{\log_2\left(\log_2(n)\right) - 1}}\right)\left(2^{2^{\log_2\left(\log_2(n)\right)}} \right) \\\\
        &= \log_2(n)\left[1 + \frac{2^{2^1}}{2^0} + \frac{2^{2^2}}{2^1} + \frac{2^{2^3}}{2^2} + \cdots + \frac{2^{2^{\log_2\left(\log_2(n)\right)}}}{2^{\log_2\left(\log_2(n)\right) - 1}}\right] \\\\
        &= \log_2(n)\left[1 + \left[\sum_{i = 1}^{\log_2\left(\log_2(n)\right)} \frac{2^{2^i}}{2^{i - 1}} \right]\right] \\\\
        &\leq \log_2(n)\left[1 + \left(\log_2\left(\log_2(n)\right)\right)\left[ \frac{2^{2^{\log_2\left(\log_2(n)\right)}}}{2^{\log_2\left(\log_2(n)\right) - 1}} \right]\right] \\\\
        &= \log_2(n)\left[1 + \left(\log_2\left(\log_2(n)\right)\right)\left[ \frac{n}{\frac{2^{\log_2\left(\log_2(n)\right)}}{2}} \right]\right] \\\\
        &= \log_2(n)\left[1 + \left(\log_2\left(\log_2(n)\right)\right)\left[ \frac{n}{\frac{\log_2(n)}{2}} \right]\right] \\\\
        &= \log_2(n)\left[1 + \left(\log_2\left(\log_2(n)\right)\right)\left[ \frac{2n}{\log_2(n)} \right]\right] \\\\
        &= \log_2(n) + 2n\left(\log_2\left(\log_2(n)\right)\right) \\\\
        &= O\left(n\log\left(\log(n)\right)\right)

    \end{align*}
$$

$$\qed$$