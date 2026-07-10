---
layout: default
title: "Lecture 12: Proofs Involving Quantifiers"
---

Generalized Particular (∀)
==========================

### Proof By Generalized Particular (∀) Template

> To prove a statement of the form ∀*x* *P(x)*, *assume* *x* is an
> *arbitrary* value (i.e. a *generalized particular*) and prove *P(x)*.
> Since *x* can represent *any* value, *P(x)* will be true *for all* *x*.

> The form of the formal proof will have the form:

> Let *x* be arbitrary.

> > \[Proof of *P(x)* goes here.\]

> Since *x* was arbitrary, therefore ∀*x* *P(x)*.

**Example 1**

> Suppose *A* and *B* are sets. Prove that if *A* ∩ *B* = *A* then *A* ⊆
*B*.

First we identify the original givens and goals

> *Givens*
>
> > *A* and *B* are sets.
>
> *Goal*
>
> > (*A* ∩ *B* = *A*) → (*A* ⊆ *B*)

Using the conditional proof technique we convert the goal as

> *Givens*
>
> > *A* and *B* are sets.
> >
> > *A* ∩ *B* = *A*
>
> *Goal*
>
> > *A* ⊆ *B*

Logically, the goal can be rewritten as ∀*x* (*x* ∈ *A* → *x* ∈ *B*)
giving

> *Givens*
>
> > *A* and *B* are sets.
> >
> > *A* ∩ *B* = *A*
>
> *Goal*
>
> > ∀*x* (*x* ∈ *A* → *x* ∈ *B*)

Since this is a universally quantified goal, we will assume that *x* is
arbitrary and again bring the left hand side of the implication to the
givens

> *Givens*
>
> > *A* and *B* are sets.
> >
> > *A* ∩ *B* = *A*
> >
> > *x* is arbitrary
> > 
> > *x* ∈ *A*
>
> *Goal*
>
> > *x* ∈ *B*

Now since *x* ∈ *A* and *A* = *A* ∩ *B* implies that *x* ∈ *A* ∩ *B* and
therefore *x* ∈ *B*. Thus since *x* was arbitrary, *every* element of
*A* is an element of *B*, i.e. *A* ⊆ *B*.

Thus the formal proof would be

> **Theorem.** Suppose *A* and *B* are sets. If *A* ∩ *B* = *A* then *A* ⊆ *B*.
>
> *Proof.* 
> > Suppose *A* ∩ *B* = *A* and let *x* ∈ *A* be arbitrary.
> > Since *A* = *A* ∩ *B* implies that *x* ∈ *A* ∩ *B*, and thus *x* ∈ *B*.
> > 

> Since *x* was an arbitrary element of *A*, therefore *A* ⊆ *B*.

Specific Particular (∃)
=======================

### Proof By Specific Particular (∃) Template

> To prove a statement of the form ∃*x* *P(x)*, *assume* a *specific
> value* for *x* and prove that *P(x)* is true for that value. Then in the
> proof let *x* equal that value and show *P(x)*. Since it is true for *at
> least one* value, ∃*x* *P(x)*.

> The form of the formal proof will have the form:

> Let *x* = (decided on value).

> > \[Proof of *P(x)* goes here.\]

> Therefore ∃*x* *P(x)*.

**Example 2**

> Suppose *x* is a real number. Prove that if *x* ≠ 1 then there is a real
> number *y* such that (*y*+1)/(*y*-2) = *x*.

First we identify the original givens and goals

> *Givens*
>
> > *x* is a real number
>
> *Goal*
>
> > (*x* ≠ 1) → ∃*y* ((*y*+1)/(*y*-2) = *x*)

First we apply the conditional proof technique to give

> *Givens*
>
> > *x* is a real number
> >
> > *x* ≠ 1
>
> *Goal*
>
> > ∃*y* ((*y*+1)/(*y*-2) = *x*)

Solving the equation in the goal for *y* gives

> *y* = (2*x*+1)/(*x*-1)

Therefore we can *assume* that *y* = (2*x*+1)/(*x*-1) as a new given

> *Givens*
>
> > *x* is a real number
> >
> > *x* ≠ 1
> >
> > *y* = (2*x*+1)/(*x*-1)
>
> *Goal*
>
> > ∃*y* ((*y*+1)/(*y*-2) = *x*)

Using the second given *x* ≠ 1 gives that *y* = (2*x*+1)/(*x*-1) is a
real number and hence we have shown that there exists at least one value
for *y*.

Thus the formal proof would be

> **Theorem.** Suppose *x* is a real number. If *x* ≠ 1 then there is a
> real number *y* such that (*y*+1)/(*y*-2) = *x*.
>
> *Proof.* 
> > Let *x* be an arbitrary real number such that *x* ≠ 1. Let
> >
> > > *y* = (2*x*+1)/(*x*-1)
> >
> > which is defined since *x* ≠ 1. Then
>
> > (*y*+1)/(*y*-2) = \[((2*x*+1)/(*x*-1)) +
> > 1\]/\[((2*x*+1)/(*x*-1))-2\]
> >
> > > = \[3*x*/(*x*-1)\]/\[3/(*x*-1)\]
> > >
> > > = *x*

> Therefore, for any real number *x* ≠ 1, there exists a real number *y* such that 
> (*y*+1)/(*y*-2) = *x*.

Givens with Quantifiers
=======================

### Proofs With Givens Containing Quantifiers Template

> To use a given of the form ∃*x* *P(x)*, *assume* a *specific value*, say
> *x*<sub>0</sub>, and add the given *P*(*x*<sub>0</sub>). This is known as *existential
> instantiation* since we know *there exists* at least one value that
> makes and *P(x)* true, and thus instantiate that value as *x*<sub>0</sub>.

> The form of the formal proof will have the form:

> Suppose ∃*x* *P(x)*. Let *x* = *x*<sub>0</sub>, then *P*(*x*<sub>0</sub>).

> > \[Proof of *Q(x)* goes here.\]

> Therefore *Q(x)*.


> To use a given of the form ∀*x* *P(x)*, *assume an arbitrary value*, say *a*, and
> add the given *P(a)*. This is known as *universal instantiation* since
> we know *P(x)* is true for *every* *x* which means it is true for *any*
> *x* so we can select an *arbitrary* value *a*.

> The form of the formal proof will have the form:

> Suppose ∀*x* *P(x)*. Let *a* be arbitrary and *x*=*a*, then *P(a)*.

> > \[Proof of *Q(x)* goes here.\]

> Therefore *Q(x)*.

**Example 3**

> Prove that if ∃*x* (*P(x)* → *Q(x)*) then ∀*x* *P(x)* → ∃*x* *Q(x)*.

First we identify the original givens and goals

> *Givens*
>
> > None.
>
> *Goal*
>
> > (∃*x* (*P(x)* → *Q(x)*)) → (∀*x* *P(x)* → ∃*x* *Q(x)*)

First we apply the conditional proof technique to give

> *Givens*
>
> > ∃*x* (*P(x)* → *Q(x)*)
>
> *Goal*
>
> > ∀*x* *P(x)* → ∃*x* *Q(x)*

Again applying the conditional proof technique for the new goal gives

> *Givens*
>
> > ∃*x* (*P(x)* → *Q(x)*)
> >
> > ∀*x* *P(x)*
>
> *Goal*
>
> > ∃*x* *Q(x)*

Thus we have an existentially quantified goal. Using *existential
instantiation* with the first given implies that there exists a
*specific* value, say *x*<sub>0</sub>, such that *P*(*x*<sub>0</sub>) → *Q*(*x*<sub>0</sub>). But since ∀*x* *P(x)*, by *universal instantiation* letting *x* = *x*<sub>0</sub> we know that *P*(*x*<sub>0</sub>). By modus ponens we can then conclude that *Q*(*x*<sub>0</sub>). Hence there is *at least* one value for which *Q(x)* is
true and therefore ∃*x* *Q(x)*.

Thus the formal proof would be

> **Theorem.** If ∃*x* (*P(x)* → *Q(x)*), then ∀*x* *P(x)* → ∃*x* *Q(x)*.
>
> *Proof.* 
> > Suppose ∃*x* (*P(x)* → *Q(x)*). Let *x* = *x*<sub>0</sub>
> > for which *P*(*x*<sub>0</sub>) → *Q*(*x*<sub>0</sub>). 
> > Furthermore, suppose ∀*x* *P(x)*, then in particular *P(x*<sub>0</sub>)
> > and since *P*(*x*<sub>0</sub>) → *Q*(*x*<sub>0</sub>) we
> > can conclude that *Q*(*x*<sub>0</sub>). Therefore since there is a value *x*
> > such that *Q(x)* we have that ∃*x* *Q(x)*. 

> Therefore ∀*x* *P(x)* → ∃*x* *Q(x)*.

**Example 4**

> Prove that if *F* is a family of sets and *A* ∈ *F* then ∩*F* ⊆ *A*.

First we identify the original givens and goals

> *Givens*
>
> > None
>
> *Goal*
>
> > (*F* is a family of sets ∧ *A* ∈ *F*) → ∩*F* ⊆ *A*

Applying the conditional proof technique gives

> *Givens*
>
> > *F* is a family of sets
> >
> > *A* ∈ *F*
>
> *Goal*
>
> > ∩*F* ⊆ *A*

The goal logically means ∀*x* (*x* ∈ ∩*F* → *x* ∈ *A*) giving

> *Givens*
>
> > *F* is a family of sets
> >
> > *A* ∈ *F*
>
> *Goal*
>
> > ∀*x* (*x* ∈ ∩*F* → *x* ∈ *A*)

Since this is a universally quantified goal, we will let *x* be
arbitrary and assume *x* ∈ ∩*F* and again separate the conditional
giving

> *Givens*
>
> > *F* is a family of sets
> >
> > *A* ∈ *F*
> >
> > *x* arbitrary
> >
> > *x* ∈ ∩*F*
>
> *Goal*
>
> > *x* ∈ *A*

Since *x* ∈ ∩*F* we know that ∀*y* ∈ *F* (*x* ∈ *y*) giving

> *Givens*
>
> > *F* is a family of sets
> >
> > *A* ∈ *F*
> >
> > *x* arbitrary
> >
> > ∀*y* ∈ *F* (*x* ∈ *y*)
>
> *Goal*
>
> > *x* ∈ *A*

Because the third given is true *for all* sets in *F*, i.e. *y* is a
universal instantiation, and *A* ∈ *F* we can let *y* = *A* giving *x* ∈
*A*.

Thus the formal proof would be

> **Theorem.** If *F* is a family of sets and *A* ∈ *F* then ∩*F* ⊆ *A*.
>
> *Proof.* 
> > Suppose *A* ∈ *F*. Furthermore, let *x* be arbitrary such
> > that *x* ∈ ∩*F*. Since *x* ∈ ∩*F* and *A* ∈ *F* means *x* ∈ *A*.

> Therefore because *x* was arbitrary, ∩*F* ⊆ *A*.
