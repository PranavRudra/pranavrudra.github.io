---
layout: post
title: Exercise 3.27 (page 59)
category: solutions-manual
displayed: false
---

## Solution:

Given that $\frac{n}{\log_2(n)} < \frac{n}{2}$ for all $n > 4$, we have

$$
    \begin{align*}
        T(n) &= T\left(\frac{n}{2}\right) + T\left(\left\lfloor \frac{n}{\log_2(n)} \right\rfloor \right) + n \\
        &\leq T\left(\frac{n}{2}\right) + T\left(\frac{n}{2}\right) + n \\
        &= 2T\left(\frac{n}{2}\right) + n
    \end{align*}
$$

which is a divide-and-conquer recurrence with $a = 2, b = 2, k = 1$. 

Hence, by the second case ($a = b^k$) of the master theorem, we know that

$$
    T(n) = O(n\log(n))
$$

Similarly,

$$
    \begin{align*}
        T(n) &= T\left(\frac{n}{2}\right) + T\left(\left\lfloor \frac{n}{\log_2(n)} \right\rfloor \right) + n \\
        &\geq T\left(\frac{n}{2}\right) + n
    \end{align*}
$$

which is a divide-and-conquer recurrence with $a = 1, b = 2, k = 1$. 

Hence, by the third case ($a < b^k$) of the master theorem, we know that

$$
    T(n) = \Omega(n)
$$

Since $\frac{n}{\log_2(n)}$ is much smaller than $\frac{n}{2}$ for large $n$, we guess that $T(n) = \Theta(n)$. That is, we guess that $O(n)$ is a tighter bound for $T(n)$ than $O(n\log(n))$. To confirm our proposition, we will prove the claim via induction; we will show that $T(n) \leq cn$ for $n \geq n_0$. 

For the base case, consider $n = 2$. 

$$
    T(2) = 2 \leq c(2) \text{ iff } c \geq 2
$$

For the inductive hypothesis (IH), assume that $\forall k < n$

$$
    T(k) \leq ck
$$

Now, for the inductive step, we must show that the claim holds for $n$.

$$
    \begin{align*}
        T(n) &= T\left(\frac{n}{2}\right) + T\left(\left\lfloor \frac{n}{\log_2(n)} \right\rfloor \right) + n \\
        &\leq \frac{cn}{2} + \frac{cn}{\log_2(n)}+ n \\
        &= n\left(1 + \frac{c}{2} + \frac{c}{\log_2(n)} \right)
    \end{align*}
$$

This is less than or equal to $cn$ if

$$
    c \geq 1 + \left(\frac{c}{2} + \frac{c}{\log_2(n)}\right) \implies \left(\frac{c}{2} - \frac{c}{\log_2(n)}\right) \geq 1 \implies c \geq \left(\frac{1}{\frac{1}{2} - \frac{1}{\log_2(n)}}\right)
$$

which suggests $c \geq 2$ iff $n > 4$. Thus, $\left[\forall n \geq 5\right]\ T(n) \leq cn$ so $T(n) = O(n)$.

However, $T(n) = \Omega(n)$ as well so we can simply write $T(n) = \Theta(n)$ (as conjectured). 

$$\qed$$