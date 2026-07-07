---
layout: post
title: "The triangle count on this page is real"
---

The background of this site is a random graph, rebuilt every time you load the page or resize the window: nodes are scattered around the hero text, and each one connects to a few of its nearest neighbors. The `▲ = n` in the corner isn't decoration — it's the number of triangles in whatever graph you happened to get.

Counting them is the classic warm-up: for each vertex $$i$$, look at pairs of its neighbors and check whether they're adjacent. With adjacency sets that's $$O\!\left(\sum_i d_i^2\right)$$, which is fine at $$n = 62$$. The linear-algebra version is prettier — if $$A$$ is the adjacency matrix, then

$$
t = \frac{\operatorname{tr}(A^3)}{6}
$$

since each closed walk of length 3 traverses a triangle, and each triangle is counted once per vertex and once per direction.

I'm planning to use this space to write about things I'm reading and thinking about — mostly algorithms and complexity, occasionally not. If a post exists, it's because I wanted to work something out by explaining it.
