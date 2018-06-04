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
  We evaluate the first statement for \(n = 1\), and find that \(1^5 - 1 = 0\). Since \(5\mid0\), the statement holds when \(n = 1\). Assuming that \(5 \mid (k^5 - k)\) for some \(k \geq 1\), we intend to show that this implies the truth of the statement for \(k + 1\), that is, that \(5 \mid ((k + 1)^5 - (k + 1))\). Now,
  \[\begin{aligned}
    (k + 1)^5 - (k + 1) &= k^5 + 5k^4 + 10k^3 + 10k^2 + 5k + 1 - k - 1\\
    &= (k^5 - k) + (5k^4 + 10k^3 + 10k^2 + 5k).
  \end{aligned}\]
  Clearly 5 divides the second addend, and by our inductive hypothesis 5 divides the first addend also. Therefore \(5 \mid (k^5 - k) \implies 5 \mid ((k + 1)^5 - (k + 1))\), and the statement is true for all natural numbers \(n\).
</div>

<div class="proof">
Let \(P\) denote the second statement, that is,
\[P(n)\colon 7 \mid (n^7 - n),\enspace\forall n \in \mathcal{N}.\]
We proceed by induction. When \(n = 1\), \(n^7 - n = 0\). Because \(7 \mid 0\), \(P(1)\) is true. We now show that \(P(k) \implies P(k + 1)\) for some natural number \(k \geq 1\). Assuming \(P(k)\), that is, that \(7 \mid (k^7 - k)\), observe that
\[\begin{aligned}
  (k + 1)^7 - (k + 1) &= k^7 + 7k^6 + 21k^5 + 35k^4 + 35k^3 + 21k^2 + 7k
  + 1 - k - 1\\
  &= (k^7 - k) + 7(k^6 + 3k^5 + 5k^4 + 5k^3 + 3k^2 + k).
\end{aligned}\]
By our inductive hypothesis, the first addend above is divisible by 7, and clearly the second addend is also divisible by 7. By the principle of mathematical induction, it follows that \(7 \mid (n^7 - n)\) for every natural \(n\).
</div>
