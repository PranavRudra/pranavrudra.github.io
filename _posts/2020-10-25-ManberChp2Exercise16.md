---
layout: post
title: Exercise 2.16 (page 32)
category: solutions-manual
displayed: false
---

## Solution:

We will induct on $n$. For the base case, let the $n = 3$ lines be $l_1, l_2, l_3$. Since the lines are in general position, no two of them are parallel. Hence, every pair of lines intersects. Let $A, B, C$ be the intersections between $\\{ l_1, l_2 \\}$, $\\{l_2, l_3\\}$, and $\\{l_1, l_3\\}$ respectively. Now, recall that no three lines in general position intersect at a common point. Therefore, $A, B, C$ are all distinct. Finally, observe that $A, B, C$ cannot be collinear. If they are, $l_1 = l_2 = l_3$ and all three are parallel to one another, which is a contradiction. Thus, we have three non collinear points $A, B, C$, which, by an elementary theorem in Euclidean geometry, enclose a triangle.

For the inductive hypothesis (IH), assume that the claim holds for $n - 1$. For the inductive step, we must show that adding the $n^{\text{th}}$ line $l_n$ does not "remove" the triangle --- say $\triangle ABC$ --- formed by $l_1, l_2, \ldots, l_{n - 1}$. Given that all $n$ lines are in general position, none of $A, B, C$ can lie on $l_n$. Otherwise, we have a contradiction since each of $A, B, C$ is an intersection of two other lines as well. Now, we have two cases: $l_n$ passes through $\triangle ABC$ (i.e. intersects the interior of exactly two of $\\{AB, AC, BC\\}$) or doesn't touch $\triangle ABC$ at all. However, in either case, $\triangle ABC$ is still a triangle region enclosed by the lines $l_1, l_2, l_3, \ldots, l_n$. 

$$\qed$$