---
layout: post
title: Exercise 2 (page 6)
category: solutions-manual
displayed: false
---

## Solution:

We start with the forward direction. By theorem $1.1.4$, $A \cap B \subseteq A$. Now, let $x$ be an element of $A$. Since $A \subseteq B$, $x \in B$. Therefore, $\left(x \in A\right) \land \left(x \in B\right)$, or, in other words, $x \in A \cap B$. Thus, we have shown $A \subseteq A \cap B$. This completes the forward direction because, by the definition of set equality, 

$$
    \left(A \subseteq A \cap B\right) \land \left(A \cap B \subseteq A\right) \implies A = A \cap B
$$

For the reverse direction, observe that by set equality, $A \subseteq A \cap B$. Then, by theorem $1.1.4$, $A \cap B \subseteq B$. Hence, $x \in A$ implies that $x \in \left(A \cap B\right)$ which in turn implies that $x \in B$. Thus, we have shown $A \subseteq B$. This completes the reverse direction and the proof.

$$\qed$$