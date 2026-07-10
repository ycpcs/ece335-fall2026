---
layout: default
title: "Lecture 13: Proofs Involving Conjunctions and Biconditionals"
---

Conjunctions
============

### Proof With Conjunctions Template

> To prove a statement of the form *P* ∧ *Q*, simply prove *P* and *Q*
> separately using the same givens. Therefore, make each statement a
> separate goal to be proven.

> The form of the formal proof will have the form:

> Suppose \[any assumptions\].

> > \[Proof of *P* goes here.\] \[Proof of *Q* goes here.\]

> Therefore, *P* ∧ *Q*.

> To use a given of the form *P* ∧ *Q*, simply make *P* and *Q* separate
> givens.

**Example 1**

> Prove that if *A* ⊆ *B* and *A* ⊆ *C* then *A* ⊆ *B* ∩ *C*.

First we identify the givens and goals (applying the conditional
strategy)

> *Givens*
>
> > *A* ⊆ *B*
> >
> > *A* ⊆ *C*
>
> *Goal*
>
> > *A* ⊆ *B* ∩ *C*

Evaluating the logical form of the goal gives ∀*x* (*x* ∈ *A* → *x* ∈
*B* ∩ *C*). Applying a universal instantiation for *x*, i.e. let *x* be
arbitrary and again separating the conditional gives

> *Givens*
>
> > *A* ⊆ *B*
> >
> > *A* ⊆ *C*
> >
> > Let *x* be arbitrary
> > 
> > *x* ∈ *A*
>
> *Goal*
>
> > *x* ∈ *B* ∩ *C*

Using the definition of intersection, the goal can be rewritten as *x* ∈
*B* ∧ *x* ∈ *C*. Therefore we can separate the conjunctive into two
goals giving

> *Givens*
>
> > *A* ⊆ *B*
> >
> > *A* ⊆ *C*
> >
> > Let *x* be arbitrary
> > 
> > *x* ∈ *A*
>
> *Goal*
>
> > *x* ∈ *B*
> >
> > *x* ∈ *C*

At this point we can prove each goal separately. First, since *x* ∈ *A*
and *A* ⊆ *B* implies that *x* ∈ *B* proving the first goal. Similarly,
since *x* ∈ *A* and *A* ⊆ *C* we know that *x* ∈ *C* proving the second
goal. Therefore *x* ∈ *B* ∧ *x* ∈ *C* which gives *x* ∈ *B* ∩ *C*.

Thus the formal proof would be

> **Theorem.** *If A* ⊆ *B and A* ⊆ *C then A* ⊆ *B* ∩ *C*.
>
> *Proof.* 
> > Let *x* be an arbitrary element of *A* and suppose *A* ⊆ *B*.
> > Then *x* ∈ *B*. Likewise, supposing that *A* ⊆ *C* means *x* ∈ *C*.
> > Since *x* ∈ *A* is arbitrary with *x* ∈ *B* and *x* ∈ *C*, we can
> > conclude that *A* ⊆ *B* ∩ *C*.

Biconditionals
==============

### Proof of Biconditional Template

> To prove a statement of the form *P* ↔ *Q*, first use the strategy for
> conjunctions for (*P* → *Q*) ∧ (*Q* → *P*) giving separate goals *P* →
> *Q* and *Q* → *P*. Since these are conditional goals, prove each
> separately by first assuming *P* and proving *Q* and then assuming *Q*
> and proving *P*.

> The form of the formal proof will have the form:

> (→) Suppose *P*.

> > \[Proof of *Q* goes here.\] 

> > Thus *P* → *Q*.

> (←) Now suppose *Q*.

> > \[Proof of *P* goes here.\] 

> > Thus *Q* → *P*.

> Therefore, *P* ↔ *Q*

> To use givens of the form *P* ↔ *Q*, separate into separate givens *P* →
> *Q* and *Q* → *P* (then typically use modus ponens or modus tollens to
> assert something about *P* and/or *Q*).

**Example 2**

> Suppose *A*, *B*, and *C* are sets. Prove that *A* ∩ (*B* \\ *C*) = (*A*
> ∩ *B*) \\ *C*.

First we interpret = as equivalency which logically means ↔. Therefore
we will prove the statement *A* ∩ (*B* \\ *C*) ↔ (*A* ∩ *B*) \\ *C*.
(Note that alternatively set equality means that each side is a subset
of the other so we could instead use the goal *A* ∩ (*B* \\ *C*) ⊆ (*A*
∩ *B*) \\ *C* and (*A* ∩ *B*) \\ *C* ⊆ *A* ∩ (*B* \\ *C*)).

> *Givens* (→)
>
> > *A* ∩ (*B* \\ *C*)
>
> *Goal*
>
> > (*A* ∩ *B*) \\ *C*

Let *x* ∈ *A* ∩ (*B* \\ *C*). Then

> *x* ∈ *A* ∧ *x* ∈ (*B* \\ *C*)
>
> *x* ∈ *A* ∧ (*x* ∈ *B* ∧ *x* ∉ *C*)

By the associative law we get

> (*x* ∈ *A* ∧ *x* ∈ *B*) ∧ *x* ∉ *C*
>
> *x* ∈ *A* ∩ *B* ∧ *x* ∉ *C*
>
> *x* ∈ (*A* ∩ *B*) \\ *C*

Which means that *A* ∩ (*B* \\ *C*) → (*A* ∩ *B*) \\ *C*

For the other implication we have

> *Givens* (←)
>
> > (*A* ∩ *B*) \\ *C*
>
> *Goal*
>
> > *A* ∩ (*B* \\ *C*)

But we see that proving this direction is identical to following the →
logic in reverse, i.e. let *x* ∈ (*A* ∩ *B*) \\ *C*

> *x* ∈ *A* ∩ *B* ∧ *x* ∉ *C*
>
> (*x* ∈ *A* ∧ *x* ∈ *B*) ∧ *x* ∉ *C*

By the associative law we have

> *x* ∈ *A* ∧ (*x* ∈ *B* ∧ *x* ∉ *C*)
>
> *x* ∈ *A* ∧ *x* ∈ (*B* \\ *C*)
>
> *x* ∈ *A* ∩ (*B* \\ *C*)

Which means that (*A* ∩ *B*) \\ *C* → *A* ∩ (*B* \\ *C*).

Therefore since we have proven both directions we conclude that *A* ∩
(*B* \\ *C*) ↔ (*A* ∩ *B*) \\ *C*.
