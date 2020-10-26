---
layout: post
title: Exercise 2.17 (page 32)
category: solutions-manual
displayed: false
---

## Solution:

We will induct on $n$. For the base case ($n = 3$), refer to the beginning of exercise [2.16]({% link _posts/2020-10-25-ManberChp2Exercise16.md %}). For the inductive hypothesis (IH), assume that the claim holds for $n - 1$. Now, for the inductive step, we must show that the $n$ lines $l_1, l_2, \ldots, l_n$ form at least $n - 2$ triangles. 

By the inductive hypothesis, we know that $l_1, l_2, \ldots, l_{n - 1}$ form at least $n - 3$ triangles. Also, since all lines are in general position, every pair of lines intersects. Hence, let $P, Q, O$ be the intersection points of $\\{l_n, l_1 \\}, \\{l_n, l_2\\}, \\{l_1, l_2 \\}$ respectively. Given that no three lines intersect at a common point, $P, Q, O$ are all distinct. Further, $P, Q, O$ cannot be collinear. If they are, $l_n = l_1 = l_2$ and all three are parallel to one another, which is a contradiction. Thus, by a theorem in elementary Euclidean geometry, $P, Q, O$ enclose a triangle. This brings the total number of triangles formed by $l_1, l_2, \ldots, l_n$ to at least $n - 3 + 1 = n - 2$.

$$\qed$$