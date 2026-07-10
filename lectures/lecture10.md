---
layout: default
title: "Lecture 10: Proof Strategies"
---

Proof Terminology
=================

### **Definitions**

> A mathematical statement, known as a *theorem*, is shown to be true
> based on *assuming* that the *hypotheses* (or *givens* or
> *preconditions*) are true and through logical deduction produce a
> *valid* argument that the *conclusion* must be true.

> The assignment of a particular set of values in a theorem is known as an
> *instance*.

> A theorem can be *disproven* through a **single** *counterexample*, i.e.
> single instance, where the assignments satisfy the hypotheses but
> produce a false conclusion.

> An *assertion* is a statement of truth which must be *justified* in the
> construction of a proof.

> An *assumption* is a statement that is used to derive what *would be*
> true **if** the assumption is true.

**Example 1**

> State what are the hypotheses and conclusion of the following conjecture
> and find a counterexample that disprove it.

> Suppose *n* is a natural number larger than 2, and *n* is not prime.
> Then 2*n*+13 is not a prime number.

The hypotheses, or givens, are what the conjecture assumes to be true. Thus
in this conjecture there are three givens related to *n*:

> -   *n* is a natural number, i.e. *n* ∈ ℕ
> -   *n* is larger than 2, i.e. *n* \> 2
> -   *n* is not a prime number, i.e. *n* = *ab* where *a*, *b* ∈ ℕ and
>     1 \< *a*, *b* \< n

The conclusion is what the conjecture proposes to be true if *n* satisfies
all the hypotheses which is

> 2*n* + 13 is not a prime number.

Consider the value *n* = 3. Then 2(3) + 13 = 19 which is prime. However,
while 3 satisfies the first two hypotheses (it is a natural number \> 2)
it does not satisfy the third (since 3 is prime). Therefore the conjecture
says nothing about the truth of the conclusion (which happens to be
false).

Consider the value *n* = 4. Then 2(4) + 13 = 21 which is not prime. In
this case, 4 satisfies all the hypotheses (since it is a natural number
that is \> 2 and not prime). The conjecture states that the conclusion
should not be prime of which 21 is not (since it is 3\*7). So this
instance *confirms* the conjecture but does **NOT** prove it.

Consider the value *n* = 8. Then 2(8) + 13 = 29 which is prime. For this
instance, 8 satisfies all the hypotheses (since it is a natural number
that is \> 2 and not prime). The conjecture states that the conclusion
should not be prime, but 29 **is** prime. Thus this instance is a
*counterexample* where all the hypotheses are satisfied yet the
conclusion is false. Therefore the conjecture is *invalid*.

Conditional Proofs
==================

### **Conditional Proof Template**

> To prove a conclusion of the form *P* → *Q*, make the *assumption* that
> *P* is true and then deduce that *Q* must be true. In other words, take
> *P* as a given and construct a valid argument with *Q* as the
> conclusion.

> The form of the formal proof will have the form:

> Suppose *P*.

> > \[Proof of *Q* goes here.\]

> Therefore, *P* → *Q*.


**Example 2**

> Suppose *a* and *b* are real numbers. Prove that if *a* \< *b* \< 0,
> then *a*<sup>2</sup> \> *b*<sup>2</sup>.

We will attempt a conditional proof by using the following givens and
goal:

> *Given*
>
> > *a*, *b* ∈ ℝ
> >
> > *a* \< *b* \< 0
>
> *Goal*
>
> > *a*<sup>2</sup> \> *b*<sup>2</sup>

Since *a* and *b* are *negative*, if we multiply an inequality by either
one we must flip the inequality sign. Thus multiplying the second given
by *a* gives

> *a*<sup>2</sup> \> *ab*

Likewise multiplying the second given by *b* gives

> *ab* \> *b*<sup>2</sup>

Thus these two assertions can be added to the list of givens

> *Given*
>
> > *a*, *b* ∈ ℝ
> >
> > *a* \< *b* \< 0
> >
> > *a*<sup>2</sup> \> *ab*
> >
> > *ab* \> *b*<sup>2</sup>
>
> *Goal*
>
> > *a*<sup>2</sup> \> *b*<sup>2</sup>

Now we can combine the third and fourth givens for

> *a*<sup>2</sup> \> *ab* \> *b*<sup>2</sup> ⇒ *a*<sup>2</sup> \> *b*<sup>2</sup>

which is the goal we were trying to show. Thus the formal proof would be

> **Theorem.** Suppose a and b are real numbers. Prove that if a \< b \<
> 0, then *a*<sup>2</sup> \> *b*<sup>2</sup>.

> *Proof.* 
> > Suppose *a* \< *b* \< 0. 
> > 
> > Multiplying the inequality *a* \< *b* by the negative number *a*,
> > we can conclude that *a*<sup>2</sup> \> *ab*, and similarly
> > multiplying by *b* we get *ab* \> *b*<sup>2</sup>.
> > 

> Therefore *a*<sup>2</sup> \> *ab* \> *b*<sup>2</sup>, so *a*<sup>2</sup> \> *b*<sup>2</sup>.
> Thus, if *a* \< *b* \< 0 then *a*<sup>2</sup> \> *b*<sup>2</sup>.

Contrapositive Proofs
=====================

### **Contrapositive Proof Template**

> Alternatively, to prove a conclusion of the form *P* → *Q*, which by
> contrapositive is logically equivalent to ¬*Q* → ¬*P* make the
> *assumption* that ¬*Q* is true (i.e. that *Q* is false) and then deduce
> that ¬*P* must be true (i.e. that *P* is false). In other words, take
> ¬*Q* as a given and construct a valid argument with ¬*P* as the
> conclusion.

> The form of the formal proof will have the form:

> Suppose *Q* is false.

> > \[Proof of ¬*P* goes here.\]

> Therefore, *P* → *Q*.

**Example 3**

> Suppose *a*, *b*, and *c* are real numbers such that *a* \> *b*. Prove that if
> *ac* ≤ *bc* then *c* ≤ 0.

For this conditional proof, the initial givens and goal

> *Given*
>
> > *a*, *b*, and *c* are real numbers
> >
> > *a* \> *b*
>
> *Goal*
>
> > *ac* ≤ *bc* → *c* ≤ 0

We could add the left hand side of the goal as an additional given,
however if we construct the contrapositive of the goal we get

> ¬(*c* ≤ 0) → ¬(*ac* ≤ *bc*)
>
> *c* \> 0 → *ac* \> *bc*

Thus adding the left hand side of the contrapositive as a given and the
right hand side as the goal

> *Given*
>
> > *a*, *b*, and *c* are real numbers
> >
> > *a* \> *b*
> >
> > *c* \> 0
>
> *Goal*
>
> > *ac* \> *bc*

Since *c* is positive, we can multiply it by both sides of the second
given without changing the inequality so

> *ac* \> *bc*

which is the goal we needed to show. Thus the formal proof would be

> **Theorem.** Suppose *a*, *b*, and *c* are real numbers such that *a* \> *b*. If *ac* ≤
*bc* then *c* ≤ 0.

> *Proof.* 
> > Suppose *c* \> 0.
> > 
> > Then we can multiply both sides of the inequality *a* \> *b* 
> > by the positive value *c* to conclude that *ac* \> *bc*.
> > 

> Therefore, by the contrapositive, if *ac* ≤ *bc* then *c* ≤ 0.
