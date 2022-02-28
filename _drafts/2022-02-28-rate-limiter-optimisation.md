---
layout: post
title:  rate limiter optimisation
date:   2022-02-28 02:06:05 +0800
author: Fang Guojian
---

$$ t = r_1, r_2, \ldots , r_n $$

$$ T: t\text{ passes rate limiting} $$

$$ r_i: request_i\text{ passes rate limiting} $$

$$ P(T) = P(R_1) \times P(R_2) \times \ldots \times P(R_n) $$

$$ P(\overline{T}) = 1 - P(R_1) \times P(R_2) \times \ldots \times P(R_n) $$

Problem:
$$ \forall P(R_i), 0 \lt P(R_i) \lt 1 \implies \forall P(R_i), P(T) \lt P(R_i) $$

Goal:
$$ \forall P(R_i), 0 \lt P(R_i) \lt 1 \implies \exists P(R_j), \forall P(R_i), P(R_i) \geq P(R_j) \land P(T) = P(R_j) $$