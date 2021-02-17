---
layout: post
title: Exercise 1 (page 8)
category: solutions-manual
displayed: false
---

## Solution:

a) Let $x$ be an element of $A$.

$$
    \begin{alignat*}{2}
        x \in A &\implies x \in B &&\text{ (since $A \subseteq B$)} \\
        &\implies x \in C &&\text{ (since $B \subseteq C$)} \\
        &\implies A \subseteq C &&\text{ (by defn. of subset)}
    \end{alignat*}
$$

$$\qed$$

b) Let $x$ be an element of $A$.

$$
    \begin{alignat*}{2}
        x \in A &\implies (x \in A) \lor (x \in B) &&\text{ (by elementary logic)} \\
        &\implies x \in A \cup B &&\text{ (by defn. of union)} \\
        &\implies A \subseteq A \cup B &&\text{ (by defn. of subset)}
    \end{alignat*}
$$

Now, let $x$ be an element of $A \cup B$

$$
    \begin{alignat*}{2}
        x \in A \cup B &\implies (x \in A) \lor (x \in B) &&\text{ (by defn. of union)} \\
        &\implies (x \in A) \lor (x \in A) &&\text{ (since $A \subseteq B$)} \\
        &\implies x \in A &&\text{ (by elementary logic)} \\
        &\implies A \cup B \subseteq A &&\text{ (by defn. of subset)}
    \end{alignat*} 
$$

Then, $(A \subseteq A \cup B) \land (A \cup B \subseteq A) \implies A = A \cup B$ by defn. of set equality.

$$\qed$$

c) Let $x$ be an element of $B \cup C$.

$$
    \begin{alignat*}{2}
        x \in B \cup C &\implies (x \in B) \lor (x \in C) &&\text{ (by elementary logic)} \\
        &\implies (x \in A) \lor (x \in C) &&\text{ (since $B \subseteq A$)} \\
        &\implies x \in A \cup C &&\text{ (by defn. of union)} \\
        &\implies (B \cup C) \subseteq (A \cup C) &&\text{ (by defn. of subset)}
    \end{alignat*}
$$

Now, let $x$ be an element of $B \cap C$

$$
    \begin{alignat*}{2}
        x \in B \cap C &\implies (x \in B) \land (x \in C) &&\text{ (by defn. of intersection)} \\
        &\implies (x \in A) \land (x \in C) &&\text{ (since $B \subseteq A$)} \\
        &\implies x \in A \cap C &&\text{ (by defn. of intersection)} \\
        &\implies (B \cap C) \subseteq (A \cap C) &&\text{ (by defn. of subset)}
    \end{alignat*} 
$$

$$\qed$$
