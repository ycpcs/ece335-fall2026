---
layout: default
title: "Lecture 17: Relations"
---

Cartesian Product
=================

> **Definition**

> Suppose *a* ∈ *A* and *b* ∈ *B*, then (*a*, *b*) is known as an *ordered
pair*.

> The *Cartesian Product* of the sets *A* and *B*, denoted *A* × *B*, is
the *set* of *all* ordered pairs (*a*, *b*) where *a* ∈ *A* and *b* ∈
*B*.

> Formally,

> *A* × *B* = {(*a*, *b*) \| *a* ∈ *A* ∧ *b* ∈ *B*}

> Furthermore, we can consider the truth set for a statement *P(x,y)* with
two free variables where *x* ∈ *A* and *y* ∈ *B* by specifying the
combinations as ordered pairs from the Cartesian product.

> *truth set of P(x,y)* = {(*a*, *b*) ∈ *A* × *B* \| *P(a,b)*}

**Example 1**

> Consider the Cartesian Product ℝ × ℝ

This Cartesian product is the set of all ordered pairs of real numbers,
thus

> ℝ × ℝ = {(*x*, *y*) \| *x* ∈ ℝ ∧ *y* ∈ ℝ}

Which geometrically represents the coordinates of points in a plane (and
hence the name *Cartesian coordinates*).

**Example 2**

> Prove *A* × (*B* ∩ *C*) = (*A* × *B*) ∩ (*A* × *C*).

Note that this means that Cartesian product distributes over
intersection.

> (→) Let (*x*, *y*) be an arbitrary element of *A* × (*B* ∩ *C*). 
> > 
> > Then *x* ∈ *A* and *y* ∈ *B* ∩ *C* ⇒ *y* ∈ *B* ∧ *y* ∈ *C*. Since *x* ∈ *A* and *y* ∈ 
> > *B* gives (*x*, *y*) ∈ *A* × *B*. Similarly since *x* ∈ *A* and *y* ∈ *C* gives (*x*, 
> > *y*) ∈ *A* × *C*. Then since (*x*, *y*) ∈ *A* × *B* and (*x*, *y*) ∈ *A* × *C* ⇒ (*x*, 
> > *y*) ∈ (*A* × *B*) ∩ (*A* × *C*).

> (←) Let (*x*, *y*) be an arbitrary element of (*A* × *B*) ∩ (*A* × *C*).
> >  
> > Then (*x*, *y*) ∈ *A* × *B* and (*x*, *y*) ∈ *A* × *C*. Hence *x* ∈ *A*, *y* ∈ *B*,
> > and *y* ∈ *C*. But then *y* ∈ *B* ∩ *C* and thus (*x*, *y*) ∈ *A* × (*B* ∩ *C*).

Relations
=========

> **Definitions**

> Suppose *A* and *B* are sets, then a set *R* ⊆ *A* × *B* is known as a *relation* from *A* to *B*.

> *Domain*
> 
> For a relation *R*, the *domain* of *R* is the set of values *a* that are in the first coordinate of the relation. Formally,
> 
> Dom(*R*) = {*a* ∈ *A* \| ∃*b* ∈ *B* ((*a*, *b*) ∈ *R*)}

> *Range*
>
> The *range* of a relation *R* is the set of values *b* that are in the second coordinate of the relation. Formally,
> 
> Range(*R*) = {*b* ∈ *B* \| ∃*a* ∈ *A* ((*a*, *b*) ∈ *R*)}

> *Inverse*
> 
> The *inverse* of a relation *R* is the set of ordered pairs (*b*, *a*) such that (*a*, *b*) is in *R*. Formally,
>
> *R* <sup>-1</sup> = {(*b*, *a*) ∈ *B* × *A* \| (*a*, *b*) ∈ *R*}

> *Composition*
>
> For two relations *R* from *A* to *B* and *S* from *B* to *C*, the *composition* is a relation from *A* to *C* given by (**note** the order of the composition)
>
> *S* ○ *R* = {(*a*, *c*) ∈ *A* × *C* \| ∃*b* ∈ *B* ((*a*, *b*) ∈ *R* ∧
> (*b*, *c*) ∈ *S*)}

**Example 3**

> Let *S* be the set of all students at YCP and *C* be the set of all YCP courses.

> Find a relation between students and courses and state the domain, range, and inverse of the relation.

We will let *E* be the relation between students and the courses they
are enrolled in. Then

> *E* = {(*s*, *c*) ∈ *S* × *C* \| *s* is enrolled in *c*}

The domain is the set of students that are currently enrolled in a
course at YCP.

> Dom(*E*) = {*s* ∈ *S* \| ∃*c* ∈ *C* ((*s*, *c*) ∈ *E*)}

The range is the set of courses that have students enrolled in them

> Range(*E*) = {*c* ∈ *C* \| ∃*s* ∈ *S* ((*s*, *c*) ∈ *E*)}

The inverse is the relation between courses and students enrolled in
them

> *E* <sup>-1</sup> = {(*c*, *s*) ∈ *C* × *S* \| (*s*, *c*) ∈ *E*}

**Example 4**

> Using the relation *E* from the previous example, determine

> *E* <sup>-1</sup> ○ *E* and *E* ○ *E* <sup>-1</sup>

For *E* <sup>-1</sup> ○ *E*, since *E* is a relation from *S* to *C* and *E* <sup>-1</sup>
is a relation from *C* to *S*, *E* <sup>-1</sup> ○ *E* will be a relation from *S*
to *S*. Thus if we let *s* and *t* be two elements of *S*, then by the
definition

> *E* <sup>-1</sup> ○ *E* = {(*s*, *t*) ∈ *S* × *S* \| ∃*c* ∈ *C* ((*s*, *c*) ∈
> *E* ∧ (*c*, *t*) ∈ *E* <sup>-1</sup>)}
>
> > = {(*s*, *t*) ∈ *S* × *S* \| ∃*c* ∈ *C* (*s* is enrolled in *c* and
> > *c* is a course that *t* is enrolled in)}
> >
> > = {(*s*, *t*) ∈ *S* × *S* \| ∃*c* ∈ *C* (both *s* and *t* are
> > enrolled in *c*)}
>
> Thus *E* <sup>-1</sup> ○ *E* are the pairs of students that are enrolled in the
> same courses.

For *E* ○ *E* <sup>-1</sup>, since *E* <sup>-1</sup> is a relation from *C* to *S* and *E*
is a relation from *S* to *C*, *E* ○ *E* <sup>-1</sup> will be a relation from *C*
to *C*. Thus if we let *c* and *d* be two elements of *C*, then by the
definition

> *E* ○ *E* <sup>-1</sup> = {(*c*, *d*) ∈ *C* × *C* \| ∃*s* ∈ *S* ((*c*, *s*) ∈
> *E* <sup>-1</sup> ∧ (*s*, *d*) ∈ *E*)}
>
> > = {(*c*, *d*) ∈ *C* × *C* \| ∃*s* ∈ *S* (*c* is a course *s* is
> > enrolled in and *s* is enrolled in course *d*)}
> >
> > = {(*c*, *d*) ∈ *C* × *C* \| ∃*s* ∈ *S* (*s* is enrolled in both *c*
> > and *d*)}
>
> Thus *E* ○ *E* <sup>-1</sup> are the pairs of courses each student is enrolled
> in.

*Properties of Relations*

Suppose *R* is a relation from *A* to *B*, *S* is a relation from *B* to
*C*, and *T* is a relation from *C* to *D*. Then the following
properties hold

> 1.  (*R* <sup>-1</sup>)<sup>-1</sup> = *R*.
> 2.  Dom(*R* <sup>-1</sup>) = Range(*R*).
> 3.  Range(*R* <sup>-1</sup>) = Dom(*R*).
> 4.  *T* ○ (*S* ○ *R*) = (*T* ○ *S*) ○ *R* (i.e. associativity for
>     composition)
> 5.  (*S* ○ *R*)<sup>-1</sup> = *R* <sup>-1</sup> ○ *S* <sup>-1</sup>.

Binary Relations
================

> **Definition**

> A relation *R* is known as a *binary relation* if the elements of the ordered pairs are drawn from the same set *A*, i.e.
> 
> *R* ⊆ *A* × *A*

We will use an alternative notation for binary relations

> (*x*, *y*) ∈ *R* ⇒ *xRy*

*Reflexive*

> *R* is said to be *reflexive* if
>
> ∀*x* ∈ *A* (*xRx*)
>
> i.e. all pairs (*x*, *x*) ∈ *R*.

*Symmetric*

> *R* is said to be *symmetric* if
>
> ∀*x* ∈ *A* ∀*y* ∈ *A* (*xRy* → *yRx*)
>
> i.e. if (*x*, *y*) ∈ *R* then (*y*, *x*) ∈ *R*.

*Transitive*

> *R* is said to be *transitive* if
> 
> ∀*x* ∈ *A* ∀*y* ∈ *A* ∀*z* ∈ *A* ((*xRy* ∧ *yRz*) → *xRz*)
> 
> i.e. if (*x*, *y*) ∈ *R* and (*y*, *z*) ∈ *R* then (*x*, *z*) ∈ *R*.

*Properties of Binary Relations*

> 1.  *R* is *reflexive* ↔ *i*<sub>A</sub> ⊆ *R* (where *i*<sub>A</sub> is the *identity
>     relation* on *A* defined as
>
>     > *i*<sub>A</sub> = {(*x*, *y*) ∈ *A* × *A* \| *x* = *y*}
>
> 2.  *R* is *symmetric* ↔ *R* = *R* <sup>-1</sup>
>
> 3.  *R* is *transitive* ↔ *R* ○ *R* ⊆ *R*

**Example 5**

> Let the set *A* = {1,2} and *B* = ℘(*A*). List the elements of the binary relation *S* defined by

> *S* = {(*x*, *y*) ∈ *B* × *B* \| *x* ⊆ *y*}

For *A* = {1,2}, *B* = ℘(*A*) = { ∅, {1}, {2}, {1,2} }.

Therefore the relation will consist of all pairs of *sets* from *B* in
which the first set is a subset of the second.

Since the emptyset is a subset of all sets (including itself), we know
that the following ordered pairs are in *S*

> (∅, ∅), (∅, {1}), (∅, {2}), (∅, {1,2})

The set {1} is a subset of itself and {1,2} so the following ordered
pairs are in *S*

> ({1}, {1}), ({1}, {1,2})

Likewise the set {2} is a subset of itself and {1,2} so the following
ordered pairs are in *S*

> ({2}, {2}), ({2}, {1,2})

Finally, the set {1,2} is only a subset of itself giving the ordered
pair

> ({1,2}, {1,2})

Thus the relation *S* has the elements

> *S* = { (∅, ∅), (∅, {1}), (∅, {2}), (∅, {1,2}), ({1}, {1}), ({1},
> {1,2}), ({2}, {2}), ({2}, {1,2}), ({1,2}, {1,2}) }

**Example 6**

> Prove *R* is *symmetric* ↔ *R* = *R* <sup>-1</sup>

> (→) Assume *R* is *symmetric* and let *xRy*.
> > 
> > Since *R* is symmetric, *xRy* ⇒ *yRx*. But for *xRy*, *yR* <sup>-1</sup>*x* and thus *R* ⊆ *R* <sup>-1</sup>.
> > 
> > Similarly, suppose *xR* <sup>-1</sup>*y*. Then *yRx* and since *R* is symmetric ⇒ *xRy* and hence *R* <sup>-1</sup> ⊆ *R*.
> > 
> > Thus since *R* ⊆ *R* <sup>-1</sup> and *R* <sup>-1</sup> ⊆ *R*, *R* = *R* <sup>-1</sup>.

> (←) Assume *R* = *R* <sup>-1</sup> and let *xRy*. 
> > 
> > Since *R* = *R* <sup>-1</sup> ⇒ *xR* <sup>-1</sup>*y* and thus *yRx*. Hence *xRy* → *yRx* which means *R* is *symmetric*.
