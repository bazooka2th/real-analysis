---
title: "&#x200b;1. Logic and Proof Techniques"
excerpt: "Proofs by induction."
tags:
  - induction
last_modified_at: 2018-06-03T15:42:13-05:00
---

> Use mathematical induction to prove that for all natural numbers \\(n\\):
> 1. \\(n^5 - n\\) is a multiple of 5, and
> 2. \\(n^7 - n\\) is a multiple of 7.

<div class="proof">
  We evaluate the first statement for \(n = 1\colon 1^5 - 1 = 0\).
  Since \(5\mid0\), the statement is true for \(n = 1\). Assume that
  \(5 \mid (k^5 - k)\) for some \(k \geq 1\). We intend to show that this
  implies the truth of the statement for \(k + 1\), that is, that
  \(5 \mid ((k + 1)^5 - (k + 1))\). Now,
  \[\begin{aligned}
    (k + 1)^5 - (k + 1) &= k^5 + 5k^4 + 10k^3 + 10k^2 + 5k + 1 - k - 1\\
    &= (k^5 - k) + (5k^4 + 10k^3 + 10k^2 + 5k).
  \end{aligned}\]
  Clearly, 5 divides the second addend, and by our inductive hypothesis
  5 divides the first addend also. Therefore \(5 \mid (k^5 - k) \implies
  5 \mid ((k + 1)^5 - (k + 1))\), and the statement is true for all
  natural numbers \(n\).
</div>
