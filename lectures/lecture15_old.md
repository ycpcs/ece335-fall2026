---
layout: default
title: "Lecture 15: Existence and Uniqueness Proofs"
---

Unique Goals
============

### Proof Of Unique Particular Template

> To prove a goal of the form ∃!*x* *P(x)*, i.e. that there is a *unique*
> *x* that makes *P(x)* true, construct two separate proofs:

> > *Existence:* Prove ∃ *x* *P(x)*.
> > *Uniqueness:* Prove ∀*y* ∀*z* ((*P(y)* ∧ *P(z)*) → *y* = *z*).

> The form of the formal proof will have the form:

> *Existence.* 

> > \[Proof of ∃ *x* *P(x)* goes here.\] 

> *Uniqueness.* 

> > \[Proof of ∀*y* ∀*z* ((*P(y)* ∧ *P(z)*) → *y* = *z*) goes here.\]

> Therefore, ∃!*x* *P(x)*.

**Example 1**

> Prove there is a unique set *A* such that for every set *B*, *A* ∪ *B* =
> *B*.

First we identify the givens and goals for the existence part

> *Givens*
>
> > *A* and *B* are sets.
>
> *Goal*
>
> > ∃!*A* (∀*B* (*A* ∪ *B* = *B*)

Since we only need to find *one* *A* that satisfies the condition *for
all* *B*, we can simply let *A* = ∅. Then clearly ∅ ∪ *B* = *B* for all
*B*. Thus *there exists* a set that is true *for all* *B*.

Next we identify the givens and goals for the uniqueness part

> *Givens*
>
> > *C* and *D* are sets
> >
> > ∀*B* (*C* ∪ *B* = *B*)
> >
> > ∀*B* (*D* ∪ *B* = *B*)
>
> *Goal*
>
> > *C* = *D*

Since the second given must be true *for all* *B*, choose *B* = *D*
giving *C* ∪ *D* = *D*. Similarly for the third given choose *B* = *C*
giving *D* ∪ *C* = *C*. Then since *D* = *C* ∪ *D* = *D* ∪ *C* = *C* we
have *C* = *D*. Thus there must be a *unique* set *for all* *B*
(assuming one exists which was shown in the previous part).

Thus the formal proof would be

> **Theorem.** *There is a unique set A such that for every set B, A* ∪
> *B = B*.
>
> *Proof.* 
> > Existence: Clearly ∀*B* (∅ ∪ *B* = *B*), thus there exists a
> > set that satisfies the required property.
>
> > Uniqueness: Let *C* and *D* be sets such that ∀*B* (*C* ∪ *B* = *B*)
> > and ∀*B* (*D* ∪ *B* = *B*). Since these conditions must hold for all
> > *B*, select *B* = *D* in the first assumption giving *C* ∪ *D* = *D*.
> > Similarly selecting *B* = *C* in the second assumption gives *D* ∪ *C*
> > = *C*. Clearly *C* ∪ *D* = *D* ∪ *C*, thus *C* = *D*.
>
> Therefore, ∅ is the unique set such that ∀*B* (∅ ∪ *B* = *B*).

Unique Givens
=============

### Proof With Unique Particular Given Template

> To use a given of the form ∃!*x* *P(x)*, i.e. that there is a *unique*
> *x* that makes *P(x)* true, use two separate givens

> - *Existence:* ∃ *x* *P(x)*. Select an *existential instantiation*
> *x*<sub>0</sub> and assert *P(x*<sub>0</sub>*)*.
>
> - *Uniqueness:* ∀*y* ∀*z* ((*P(y)* ∧ *P(z)*) → *y* = *z*). If during
> the proof you can show *P(y)* and *P(z)* are both true, then you can
> assert *y* = *z*.

**Example 2**

> Suppose *A*, *B*, and *C* are sets. *A* and *B* are not disjoint, *A*
> and *C* are not disjoint, and *A* has exactly one element. Prove that
> *B* and *C* are not disjoint.

First we identify the givens and goals

> *Givens*
>
> > *A* ∩ *B* ≠ ∅
> >
> > *A* ∩ *C* ≠ ∅
> >
> > ∃!*x* (*x* ∈ *A*)
>
> *Goal*
>
> > *B* ∩ *C* ≠ ∅

Translating all the statements using quantifiers gives

> *Givens*
>
> > ∃*x* (*x* ∈ *A* ∩ *B*)
> >
> > ∃*x* (*x* ∈ *A* ∩ *C*)
> >
> > ∃*x* (*x* ∈ *A*)
> >
> > ∀*y* ∀*z* (*y* ∈ *A* ∧ *z* ∈ *A* → *y* = *z*)
>
> *Goal*
>
> > ∃*x* (*x* ∈ *B* ∩ *C*)

Applying the definition of intersection to the first two givens and the
goal then gives

> *Givens*
>
> > ∃*x* (*x* ∈ *A* ∧ *x* ∈ *B*)
> >
> > ∃*x* (*x* ∈ *A* ∧ *x* ∈ *C*)
> >
> > ∃*x* (*x* ∈ *A*)
> >
> > ∀*y* ∀*z* (*y* ∈ *A* ∧ *z* ∈ *A* → *y* = *z*)
>
> *Goal*
>
> > ∃*x* (*x* ∈ *B* ∧ *x* ∈ *C*)

We can now apply existential instantiation to the first two givens by
letting *x* = *a* for the first given and *x* = *b* for the second given
(note that we must use different particulars since we cannot assume they
are the same element). Thus we can also remove the third given since it
is redundant, giving

> *Givens*
>
> > *a* ∈ *A*
> >
> > *a* ∈ *B*
> >
> > *b* ∈ *A*
> >
> > *b* ∈ *C*
> >
> > ∀*y* ∀*z* (*y* ∈ *A* ∧ *z* ∈ *A* → *y* = *z*)
>
> *Goal*
>
> > ∃*x* (*x* ∈ *B* ∧ *x* ∈ *C*)

At this point we observe that since *a* ∈ *A* and *b* ∈ *A*, by the last
given we can assert that *a* = *b*. Therefore we get that *b* ∈ *B* and
*b* ∈ *C* which means there exists an element in their intersection and
thus *B* and *C* are not disjoint.

Thus the formal proof would be

> **Theorem.** Suppose A, B, and C are sets. Furthermore, suppose A and
> B are not disjoint, A and C are not disjoint, and A has exactly one
> element. Then B and C are not disjoint.
>
> *Proof.* 
> > Since *A* and *B* are not disjoint, let *a* be an element
> > such that *a* ∈ *A* and *a* ∈ *B*. Similarly since *A* and *C* are not
> > disjoint, let *b* be an element such that *b* ∈ *A* and *b* ∈ *C*.
> > Since *A* has *exactly* one element and *a* ∈ *A* and *b* ∈ *A*, we
> > can conclude that *a* = *b*. But then *b* ∈ *B* and *b* ∈ *C* so
> > therefore *b* ∈ *B* ∩ *C*, and thus *B* and *C* are not disjoint.
