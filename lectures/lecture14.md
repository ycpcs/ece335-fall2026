---
layout: default
title: "Lecture 14: Proofs Involving Disjunctions"
---

Disjunction Givens
==================

### Proof With Disjunctive Givens Template

> To use a given of the form *P* ∨ *Q*, create two cases:

> > *Case 1:* Assume *P* is true and prove the goal.

> > *Case 2:* Assume *Q* is true and prove the goal.

> Then since one (or both) of *P* or *Q* must be true, the goal will have
> to be true.

> The form of the formal proof will have the form:

> *Case 1.* Suppose *P* is true.

> > \[Proof of goal goes here.\]

> *Case 2.* Suppose *Q* is true.

> > \[Proof of goal goes here.\]

> Since *P* ∨ *Q* covers all the possibilities, the goal must be true.

> Alternatively, to use a given of the form *P* ∨ *Q*, if ¬*P* (or ¬*Q*)
> can be shown, then *Q* (or *P*) can be asserted.

**Example 1**

> Suppose *A*, *B*, and *C* are sets. Prove that *A* ∩ (*B* ∪ *C*) ⊆ (*A*
> ∩ *B*) ∪ *C*.

First we identify the givens and goals (applying the conditional
strategy)

> *Givens*
>
> > *A*, *B*, and *C* are sets.
>
> *Goal*
>
> > *A* ∩ (*B* ∪ *C*) ⊆ (*A* ∩ *B*) ∪ *C*

Evaluating the logical form of the goal gives ∀*x* (*x* ∈ *A* ∩ (*B* ∪
*C*) → *x* ∈ (*A* ∩ *B*) ∪ *C*). Applying a universal instantiation for
*x*, i.e. let *x* be arbitrary and again separating the conditional
gives

> *Givens*
>
> > *A*, *B*, and *C* are sets.
> >
> > Let *x* be arbitrary
> > 
> > *x* ∈ *A* ∩ (*B* ∪ *C*)
>
> *Goal*
>
> > *x* ∈ (*A* ∩ *B*) ∪ *C*

Using the definition of intersection, the second given can be rewritten
as *x* ∈ *A* ∧ *x* ∈ *B* ∪ *C*. Therefore we can separate the
conjunctive into two givens giving

> *Givens*
>
> > *A*, *B*, and *C* are sets.
> >
> > Let *x* be arbitrary
> > 
> > *x* ∈ *A*
> >
> > *x* ∈ *B* ∪ *C*
>
> *Goal*
>
> > *x* ∈ (*A* ∩ *B*) ∪ *C*

Now we can apply the definition of union to the third given which gives

> *Givens*
>
> > *A*, *B*, and *C* are sets.
> >
> > Let *x* be arbitrary
> > 
> > *x* ∈ *A*
> >
> > (*x* ∈ *B*) ∨ (*x* ∈ *C*)
>
> *Goal*
>
> > *x* ∈ (*A* ∩ *B*) ∪ *C*

At this point we have a disjunction in the last given so we will break
it up into two cases:

> *Case 1:* Assume *x* ∈ *B*. Then since *x* ∈ *A* means that *x* ∈ *A* ∩
> *B* and thus *x* ∈ (*A* ∩ *B*) ∪ *C*.

> *Case 2:* Assume *x* ∈ *C*. Then we immediately see *x* ∈ (*A* ∩ *B*) ∪
> *C*.

Since *x* was arbitrary, in either case we get *A* ∩ (*B* ∪ *C*) ⊆ (*A*
∩ *B*) ∪ *C*.

Thus the formal proof would be

> **Theorem.** *Suppose A, B, and C are sets. Prove that A* ∩ *(B* ∪
> *C)* ⊆ *(A* ∩ *B)* ∪ *C*.
>
> *Proof.* 
> > Suppose *x* is arbitrary such that *x* ∈ *A* ∩ (*B* ∪ *C*).
> > Then *x* ∈ *A*, and *x* ∈ *B* or *x* ∈ *C*. Thus consider two cases:
> > 
> > *Case 1.* Suppose *x* ∈ *B*. Then since *x* ∈ *A* means that *x* ∈ *A*
> > ∩ *B* and therefore *x* ∈ (*A* ∩ *B*) ∪ *C*.
> >
> > *Case 2.* Suppose *x* ∈ *C*. Then clearly *x* ∈ (*A* ∩ *B*) ∪ *C*.
> >
> Since *x* was arbitrary, we can conclude that *A* ∩ (*B* ∪ *C*) ⊆ (*A*
> ∩ *B*) ∪ *C*.

Disjunction Goals
=================

### Proof With Disjunction Goals Template

> **Strategy 1**

> To prove a statement of the form *P* ∨ *Q*, break the proof up into
> cases and prove either *P* or *Q* for each case. Then argue that the
> cases cover all possibilities.

> The form of the formal proof will have the form:

> Suppose \[any assumptions\].

> > *Case 1.* \[Proof of *P* goes here.\] 

> > *Case 2.* \[Proof of *Q* goes here.\] 

> Therefore since the cases cover all possibilities, *P* ∨ *Q*.

> **Strategy 2**

> To prove a statement of the form *P* ∨ *Q*, assume *P* is false (since
> if *P* is true then the goal is true) and prove *Q*.

> The form of the formal proof will have the form:

> If *P* is true, then clearly *P* ∨ *Q* is true. Thus suppose ¬*P*.

> > \[Proof of *Q* goes here.\]

> Therefore, *P* ∨ *Q*.

**Example 2**

> Suppose *A*, *B*, and *C* are sets. Prove that *A* \\ (*B* \\ *C*) ⊆
(*A* \\ *B*) ∪ *C*.

First we identify the givens and goals (applying the conditional
strategy)

> *Givens*
>
> > *A*, *B*, and *C* are sets
>
> *Goal*
>
> > *A* \\ (*B* \\ *C*) ⊆ (*A* \\ *B*) ∪ *C*

Using subset and universal instantiation, we can rewrite the givens and
goal as

> *Givens*
>
> > *A*, *B*, and *C* are sets
> >
> > *x* ∈ *A* \\ (*B* \\ *C*)
>
> *Goal*
>
> > *x* ∈ (*A* \\ *B*) ∪ *C*

Then applying the definition of union transforms the goal into

> *Givens*
>
> > *A*, *B*, and *C* are sets
> >
> > *x* ∈ *A* \\ (*B* \\ *C*)
>
> *Goal*
>
> > *x* ∈ (*A* \\ *B*) ∨ *x* ∈ *C*

Manipulating the second given using the definition of set difference
gives

> *Givens*
>
> > *A*, *B*, and *C* are sets
> >
> > *x* ∈ *A*
> >
> > *x* ∉ (*B* \\ *C*)
>
> *Goal*
>
> > *x* ∈ (*A* \\ *B*) ∨ *x* ∈ *C*

And subsequently applying the definition of set difference to the last
given (noting that *x* ∉ (*B* \\ *C*) ⇒ ¬(*x* ∈ *B* \\ *C*) ⇒ ¬(*x* ∈
*B* ∧ *x* ∉ *C*) which by DeMorgan's Law gives (*x* ∉ *B* ∨ *x* ∈ *C*)

> *Givens*
>
> > *A*, *B*, and *C* are sets
> >
> > *x* ∈ *A*
> >
> > *x* ∉ *B* ∨ *x* ∈ *C*
>
> *Goal*
>
> > *x* ∈ (*A* \\ *B*) ∨ *x* ∈ *C*

At this point we will begin to consider separate cases to prove each of
the parts of the goal

> *Case 1:* Assume *x* ∉ *B*. Since *x* ∈ *A* means *x* ∈ *A* \\ *B*
> proving the first part of the goal.

> *Case 2:* Assume *x* ∈ *C*. Then clearly *x* ∈ *C* proving the second
> part of the goal.

Therefore in either case one of the two goals was proven, and since *x*
was arbitrary *A* \\ (*B* \\ *C*) ⊆ (*A* \\ *B*) ∪ *C*.

Thus the formal proof would be

> **Theorem.** *Suppose A, B, and C are sets. Prove that A \\ (B \\ C)*
> ⊆ *(A \\ B)* ∪ *C*.
>
> *Proof.* 
> > Suppose *x* is arbitrary such that *x* ∈ *A* \\ (*B* \\ *C*).
> > Thus *x* ∈ *A*, and *x* ∉ *B* or *x* ∈ *C*. Consider two cases
> > separately,
> > 
> > *Case 1.* Suppose *x* ∉ *B*. Then since *x* ∈ *A* means that *x* ∈
> > (*A* \\ *B*) ∪ *C*.
> >
> > *Case 2.* Suppose *x* ∈ *C*. Immediately we have *x* ∈ (*A* \\ *B*) ∪
> > *C*.
> >
> Since *x* was arbitrary, we can conclude that *A* ∩ *A* \\ (*B* \\ *C*)
> ⊆ (*A* \\ *B*) ∪ *C*.

**Example 3**

> Suppose *F* and *G* are families of sets. Prove ∪(*F* ∪ *G*) = (∪*F*) ∪
> (∪*G*).

First we identify the givens and goals (converting = to ↔)

> *Givens*
>
> > *F* and *G* are families
>
> *Goal*
>
> > *x* ∈ ∪(*F* ∪ *G*) ↔ *x* ∈ (∪*F*) ∪ (∪*G*)

Separating the biconditional into two goals gives

> *Givens*
>
> > *F* and *G* are families
>
> *Goal*
>
> > *x* ∈ ∪(*F* ∪ *G*) → *x* ∈ (∪*F*) ∪ (∪*G*)
> >
> > *x* ∈ ∪(*F* ∪ *G*) ← *x* ∈ (∪*F*) ∪ (∪*G*)

Thus we will prove each direction individually. For the first goal we
can write

> *Givens* (→)
>
> > *F* and *G* are families
> >
> > *x* ∈ ∪(*F* ∪ *G*)
>
> *Goal* (→)
>
> > *x* ∈ (∪*F*) ∪ (∪*G*)

Expanding the given using the definition of family union gives

> *Givens* (→)
>
> > *F* and *G* are families
> >
> > ∃ *A* ∈ (*F* ∪ *G*) (*x* ∈ *A*)
>
> *Goal* (→)
>
> > *x* ∈ (∪*F*) ∪ (∪*G*)

We now apply existential instantiation to the given by letting the set
*A*<sub>0</sub> be the set containing *x* thus

> *Givens* (→)
>
> > *F* and *G* are families
> >
> > *A*<sub>0</sub> ∈ (*F* ∪ *G*)
> >
> > *x* ∈ *A*<sub>0</sub>
>
> *Goal* (→)
>
> > *x* ∈ (∪*F*) ∪ (∪*G*)

Finally we can apply the definition of union to the second given giving
the disjunction

> *Givens* (→)
>
> > *F* and *G* are families
> >
> > *A*<sub>0</sub> ∈ *F* ∨ *A*<sub>0</sub> ∈ *G*
> >
> > *x* ∈ *A*<sub>0</sub>
>
> *Goal* (→)
>
> > *x* ∈ (∪*F*) ∪ (∪*G*)

Now consider two cases

> *Case 1a:* Suppose *A*<sub>0</sub> ∈ *F*. Then since *x* ∈ *A*<sub>0</sub> means that
> *x* ∈ ∪*F* and therefore *x* ∈ (∪*F*) ∪ (∪*G*).
>
> *Case 2a:* Suppose *A*<sub>0</sub> ∈ *G*. Then similarly since *x* ∈ *A*<sub>0</sub>
> means that *x* ∈ ∪*G* and therefore *x* ∈ (∪*F*) ∪ (∪*G*).

Thus we have *x* ∈ ∪(*F* ∪ *G*) → *x* ∈ (∪*F*) ∪ (∪*G*).

For the original second goal we can write

> *Givens* (←)
>
> > *F* and *G* are families
> >
> > *x* ∈ (∪*F*) ∪ (∪*G*)
>
> *Goal* (←)
>
> > *x* ∈ ∪(*F* ∪ *G*)

Applying the definition of union to the second given gives the
disjunction

> *Givens* (←)
>
> > *F* and *G* are families
> >
> > *x* ∈ ∪*F* ∨ *x* ∈ ∪*G*
>
> *Goal* (←)
>
> > *x* ∈ ∪(*F* ∪ *G*)

Now consider two cases

> *Case 1b:* Suppose *x* ∈ ∪*F*. Then ∃ *A* ∈ *F* (*x* ∈ *A*) so let *A*
> = *A*<sub>0</sub> giving *A*<sub>0</sub> ∈ *F* and *x* ∈ *A*<sub>0</sub>.
> Since *A*<sub>0</sub> ∈ *F* we know that *A*<sub>0</sub> ∈ *F* ∪ *G* and 
> therefore because *x* ∈ *A*<sub>0</sub> gives ∃ *A* ∈ (*F* ∪ *G*) (*x* ∈ *A*). 
> But this implies that *x* ∈ ∪(*F* ∪ *G*).
>
> *Case 2b:* Suppose *x* ∈ ∪*G*. Then similarly ∃ *A* ∈ *G* (*x* ∈ *A*)
> so let *A* = *A*<sub>1</sub> giving *A*<sub>1</sub> ∈ *G* and *x* ∈ *A*<sub>1</sub>.
> Since *A*<sub>1</sub> ∈ *G* we know that *A*<sub>1</sub> ∈ *F* ∪ *G* and therefore
> because *x* ∈ *A*<sub>1</sub> gives ∃ *A* ∈ (*F* ∪ *G*) (*x* ∈ *A*). 
> But this implies that *x* ∈ ∪(*F* ∪ *G*).

Thus we have *x* ∈ ∪(*F* ∪ *G*) ← *x* ∈ (∪*F*) ∪ (∪*G*).

Thus the formal proof would be

> **Theorem.** *Suppose F and G are families of sets. Then* ∪*(F* ∪ *G)
> = (*∪*F)* ∪ *(*∪*G)*.
>
> *Proof.* 
> > (→) Suppose *x* ∈ ∪(*F* ∪ *G*). Then there exists a set
> > *A*<sub>0</sub> such that *A*<sub>0</sub> ∈ (*F* ∪ *G*) 
> > with *x* ∈ *A*<sub>0</sub>.
> >
> > Since *A*<sub>0</sub> ∈ (*F* ∪ *G*) 
> > we know that *A*<sub>0</sub> ∈ *F* or *A*<sub>0</sub> ∈ *G*. 
> > Consider two cases separately,
> > 
> > > *Case 1:* Suppose *A*<sub>0</sub> ∈ *F*. Then since *x* ∈ *A*<sub>0</sub> 
> > > means that *x* ∈ ∪*F* and therefore *x* ∈ (∪*F*) ∪ (∪*G*).
> > >
> > > *Case 2:* Suppose *A*<sub>0</sub> ∈ *G*. Then similarly since
> > >  *x* ∈ *A*<sub>0</sub> means that *x* ∈ ∪*G* and therefore *x* ∈ (∪*F*) ∪ (∪*G*).
> >
> > Thus since either *x* ∈ ∪*F* or *x* ∈ ∪*G* we conclude that *x* ∈
> > (∪*F*) ∪ (∪*G*).
> >
> > (←) Now suppose *x* ∈ (∪*F*) ∪ (∪*G*). Then *x* ∈ (∪*F*) or *x* ∈
> > (∪*G*). Consider two cases separately,
> > 
> > > *Case 1:* Suppose *x* ∈ ∪*F*. Then there exists *A*<sub>0</sub> such that
> > > *A*<sub>0</sub> ∈ *F* and *x* ∈ *A*<sub>0</sub>. Since *A*<sub>0</sub> ∈ *F* 
> > > we know that *A*<sub>0</sub> ∈ *F* ∪ *G* and therefore because
> > > *x* ∈ *A*<sub>0</sub> gives ∃ *A* ∈ (*F* ∪ *G*) (*x* ∈ *A*). 
> > > But this implies that *x* ∈ ∪(*F* ∪ *G*).
> > > 
> > > *Case 2:* Suppose *x* ∈ ∪*G*. Then similarly there exists *A*<sub>1</sub>
> > > such that *A*<sub>1</sub> ∈ *G* and *x* ∈ *A*<sub>1</sub>. 
> > > Since *A*<sub>1</sub> ∈ *G* we know that *A*<sub>1</sub> ∈ *F* ∪ *G* 
> > > and therefore because *x* ∈ *A*<sub>1</sub> gives ∃ *A* ∈ (*F* ∪ *G*) (*x* ∈ *A*).
> > > But this implies that *x* ∈ ∪(*F* ∪ *G*).
> >
> > Thus in either case *x* ∈ ∪(*F* ∪ *G*).
