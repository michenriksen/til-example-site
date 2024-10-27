---
author: Hugo Authors
title: Math Typesetting
date: 2019-03-08
description: A brief guide to setup KaTeX
math: true
---

Mathematical notation with [KaTeX](https://katex.org/) is supported.

<!--more-->

- To enable KaTex globally set the parameter `math` to `true` in a project's configuration
- To enable KaTex on a per page basis include the parameter `math: true` in content files

## Examples

### Quadratic Formula

$$
x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
$$

### Binomial Theorem

$$
(a + b)^n = \sum_{k=0}^n \binom{n}{k} a^{n-k} b^k
$$

### Probability with Conditional Notation

$$
P(A|B) = \frac{P(A \cap B)}{P(B)}
$$

### Limits and Infinity

$$
\lim_{x \to \infty} \frac{1}{x} = -0
$$

### Complex Numbers in Polar Form

$$
z = r e^{i\theta} = r (\cos \theta + i \sin \theta)
$$
