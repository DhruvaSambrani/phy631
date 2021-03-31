---
title: Information-Theoretic Bell Inequalities
author: Dhruva Sambrani
subtitle: QCQI Phy631 Term Paper
width: 1190
history: false
---

# Local Realism

## Locality

It is the belief that systems which are "far away" in space from our system will have no effect.

This assumption is the first assumption in Special Relativity too. This leads to a finite speed for causality to travel, which is the speed of light.

Philosophically too this seems to be a requirement of basic Physics, after all, what is the use of any of our laws if another particle on the other side of the universe can affect your particle.

## Realism

This is the assumption that objects have properties whether or not said properties are measured. Is the moon there if you are not looking at it?

This too has philosophical implications. If no property of an object is real and is instead only an outcome of our measurement, what are we describing in Physics?
Isn't the world then dependant on the observer and not the observed?

# Some Mathematical formalism

## Bayes' Theorem

$$p(a,b) = p(a|b)p(b) = p(b|a)p(a)$$

## Information

$$\mathcal I(p) = -\log(p)$$
$$\mathcal I(p(a,b)) = -\log(p(a,b))$$
$$\mathcal I(p(b)) = -\log(p(b))$$
$$\mathcal I(p(a|b)) = -\log(p(a|b))$$

---

Then, from Bayes' Theorem,

$$-\log p(a,b) = -\log (p(a|b)p(b)) = -\log(p(b|a)p(a))$$
$$\implies \mathcal I(a,b) = \mathcal I(a|b)+\mathcal I(b) = \mathcal I(b|a) +\mathcal I(a)$$

## Mean information

$$\mathcal H(A,B) = \sum_{a,b}p(a,b)\mathcal I(a,b)$$

This is the Shannon Entropy!

---

Similar to the Information Bayes' Theorem,

$$\mathcal{H}(A,B) = \mathcal H (A|B) + \mathcal{H}(B)=\mathcal H(B|A) + \mathcal H(A)$$

## Mutual Information

$$\mathcal I(a;b) = \mathcal I(a) - \mathcal I(a|b) = \mathcal I(b) - \mathcal I(b|a) = \mathcal I(b;a)$$

$$\mathcal H(A;B) = \mathcal H(A) - \mathcal H(A|B) = \mathcal H(B) - \mathcal H(B|A) = \mathcal H(B;A)$$

## Two Inequalities of Information Theory

$$\mathcal H(A | B) \le \mathcal H(A) \le \mathcal H(A, B)$$

The left-hand inequality means that removing a condition never decreases the information carried by a quantity. The right-hand inequality means that two quantities never carry less information
than either quantity carries separately.

# Bell's Inequality

**The simplest one**

## Setup

Consider two systems, $\mathcal A$ and $\mathcal{B}$, with the set of measurable quantities $A$ and $A'$, and, $B$ and $B'$ respectively.

$A$ and $A'$ (and by extension, $B$ and $B'$) may not, in general, commute, so cannot be measured simultaneously. Hence a run of the experiment will involve measuring **only one** of either $A$ or $A'$.

Further, also assume that the systems $\mathcal{A}$ and $\mathcal{B}$, are "far away" in space.

## Properties of Observables

This proof of no hidden variable theory being able to explain Quantum Mechanics is one by contradiction.

Let us assume the observables($A$ and its friends) are all real and local. To recap, this means that the systems "actually" have a value for each property. That is $\mathcal{A}$ _is_ $|a, a'\rangle$[^1](and similarly for $\mathcal B$).

Further, any measurements on $\mathcal{A}$ should not effect $\mathcal{B}$ and vice versa, as these systems are well separated and properties are local.

[^1]: Abuse of notation - While normally, $|a, a'\rangle$ is used to denote a _simulataneous_ eigenvector, here, we're using it to represent a state which "actually" has $a$ and $a'$ as values for $A$ and $A'$

## What we know

1. Though we can not measure $A$ and $A'$ separately, we know $p(a,a',b,b')$ from which follow the pairwise probabilities, for eg., $p(a,b) = \sum_{a',b'}p(a,a',b,b')$
2. $p(a) = \sum_{b}p(a,b)$, $p(b|a) = p(a,b)/p(a)$

## How do we find out what we want to know

1. Run this experiment with a physical system
2. Measure $p(b|a)$
3. Check if the conditional statistics of $B$ is predicted by $p(b|a)$
   1. If it is able to, then the observables are local and objective
   2. If it is unable to, then the observables are either not local or not objective or neither

## More math

**A secret tool to help us later**

[This](#two-inequalities-of-information-theory) equation can be generalized to

$$\begin{aligned}
    \mathcal H(A,B) \le&\  \mathcal{H}(A, B', A', B)\\
    =&\ \mathcal{H}(A|B',A',B)+\mathcal{H}(B'|A',B)\\
    &+\mathcal{H}(A'|B)+\mathcal{H}(B)
\end{aligned}$$
