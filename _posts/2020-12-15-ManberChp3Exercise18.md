---
layout: post
title: Exercise 3.18 (page 58)
category: solutions-manual
displayed: false
---

## Solution:

We solve the recurrence for a few values of $n$ to get a feel for it.

$$
    \begin{align*}
        T(2) &= 1 \\
        T(4) &= 2T(2) + 1 = 3 \\
        T(8) &= 2T(4) + 1 = 7 \\
        T(16) &= 2T(8) + 1 = 15
    \end{align*}
$$

Hence, we propose that $T(n) = n - 1$. We can prove this via induction.

For the base case, consider $n = 2$. 

$$
    T(2) = 2 - 1 = 1
$$

For the inductive hypothesis (IH), assume $\forall k < n$

$$
    T(k) = k - 1
$$

Now, for the inductive step, we must show the claim holds for $n$.

$$
    \begin{alignat*}{2}
        T(n) &= 2T\left(\frac{n}{2}\right) + 1 &&\text{ (by definition of $T(n)$)} \\
        &= 2\left(\frac{n}{2} - 1\right) + 1 &&\text{ (by IH)} \\
        &= n - 1
    \end{alignat*}
$$

The text's attempt to show that $T(n) = O(n)$ by guessing $T(n) \leq cn$ fails because $cn$ is not a tight upper bound. As a result, we can only prove that $T(n) \leq cn + 1$ when trying to prove this guess via induction (try to do so yourself). To circumvent this issue, we can show that $T(n) \leq c_1n - c_2$ for constants $c_1$, $c_2$. Alternatively, we can define a new recurrence $S(n)$ such that $T(n) \leq S(n)$ and prove that $S(n) = O(n)$; this lets us conclude that $T(n)$ is also bounded above by $O(n)$. Try both options yourself.

$$\qed$$