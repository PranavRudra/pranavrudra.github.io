---
layout: post
title: Exercise 3.10 (page 57)
category: solutions-manual
displayed: false
---

## Solution:

The given "proof" is invalid since it assumes that each of the two subtrees only has single leaf node. However, in a complete binary tree, every node in the lowest level is a leaf node. Given that a complete binary subtree with $n$ total nodes will have $\left \lceil \frac{n}{2} \right \rceil$ total leaves and $\left \lfloor \frac{n}{2} \right \rfloor$ total internal nodes, the total running time for the algorithm should be

$$
    c\left \lfloor \frac{n}{2} \right \rfloor + O(k)\left \lceil \frac{n}{2} \right \rceil = O(n + nk) = O(nk) \text{ (by lemma $3.2$)}
$$

$$\qed$$