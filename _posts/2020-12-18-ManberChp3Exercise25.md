---
layout: post
title: Exercise 3.25 (page 59)
category: solutions-manual
displayed: false
---

## Solution:

Given that $\sqrt{n} < \frac{n}{2}$ for all $n > 4$, we have

$$
    \begin{align*}
        T(n) &= T\left(\frac{n}{2}\right) + T\left(\lfloor\sqrt{n}\rfloor\right) + n \\
        &\leq T\left(\frac{n}{2}\right) + T\left(\frac{n}{2}\right) + n \\
        &= 2T\left(\frac{n}{2}\right) + n
    \end{align*}
$$

which is a divide-and-conquer recurrence with $a = 2, b = 2, k = 1$. 

Hence, by the second case ($a = b^k$) of the master theorem, we know that

$$
    T(n) = O(n\log(n))
$$

However, since $\sqrt{n}$ is much smaller than $\frac{n}{2}$ for large $n$, $O(n\log(n))$ might not be the tighest upper bound on the recurrence. To find a tighter one, we can guess and check different bounds, say $T(n) = O(n)$, via induction. We shall try this approach now by attempting to show that $T(n) \leq cn$ for $n \geq n_0$. 

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
        T(n) &= T\left(\frac{n}{2}\right) + T\left(\lfloor\sqrt{n}\rfloor\right) + n \\
        &\leq \frac{cn}{2} + c\sqrt{n} + n \\
        &= n\left(1 + \frac{c}{2} + \frac{c}{\sqrt{n}} \right)
    \end{align*}
$$

This is less than or equal to $cn$ if

$$
    c \geq 1 + \left(\frac{c}{2} + \frac{c}{\sqrt{n}}\right) \implies \left(\frac{c}{2} - \frac{c}{\sqrt{n}}\right) \geq 1 \implies c \geq \left(\frac{1}{\frac{1}{2} - \frac{1}{\sqrt{n}}}\right)
$$

which suggests $c \geq 2$ iff $n > 4$. Thus, $\left[\forall n \geq 5\right]\ T(n) \leq 2n$ so $T(n) = O(n)$.

$$\qed$$