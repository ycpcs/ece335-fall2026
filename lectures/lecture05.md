---
layout: default
title: "Lecture 5: Quantifiers"
---

Universal Quantifier (∀ - for all)
==================================

> **Definition**

> > If *P(x)* is true *for all* values of *x*, we write ∀*x* (*P(x)*)
> > where ∀ is the *universal quantifier*.

**Example 1**

    M(x): "x is a man". 
    B(X): "x has brown hair."
    
    ∀x (M(x) → B(x))

Literal translation gives

*For all* people, *if* a person is a man, *then* the person has brown
hair.

    All men have brown hair.

**Example 2**

    Everything in that store is either overpriced or poorly made.

> *S(x)*: "*x* is in the store."

> *O(x)*: "*x* is fairly priced."

> *P(x)*: "*x* is well made."

"Everything" in this context has the meaning of "for all" so the
statement means that *if* the item is in the store, *then* it is
overpriced or poorly made. Thus symbolically

    ∀x (S(x) → (¬O(x) ∨ ¬P(x)))

Existential Quantifier (∃ - there exists)
=========================================

> **Definition**

> > If *P(x)* is true *for at least one* values of *x* (i.e. *there
> > exists* an *x* for which *P(x)* is true), we write ∃*x* (*P(x)*) where
> > ∃ is the *existential quantifier*.

**Example 3**

    Nobody's perfect.

> *P(x)*: "*x* is perfect."

At first glance "nobody" would seem to indicate a negated universal,
but the statement really means "there does *not* exist *a* person that
is perfect." Hence in this context "nobody" refers to an existential
giving

    ¬(∃x (P(x)))

**Example 4**

    M(x): "x is a man." R(x): "x has red hair."
    
    ∃x (M(x) ∧ B(x))

Literal translation gives

> "There exists a person such that the person is a man and the person
> has red hair."

Simplifying gives

    Some men have red hair.

Multiple Quantifiers
====================

**Example 5**

    If anyone in the the dorm has a friend who has the measles,
    then everyone in the dorm will have to be quarantined.

> *D(x)*: "*x* lives in the dorm."

> *F(y,x)*: "*y* is a friend of *x*."

> *M(y)*: "*y* has the measles."

> *Q(z)*: "*z* has to be quarantined."

In this case, "anyone" means "someone" and hence represents an
existential quantifier. "Everyone" represents a universal quantifier.
Initially we can translate as

> (Someone that lives in the dorm has someone that is a friend and whose
> friend has the measles) → (For all people, if the person lives in the
> dorm, then the person will have to be quarantined.)

The first clause symbolically becomes

> ∃*x* (*D(x)* ∧ ∃*y* (*F(y,x)* ∧ *M(y)*))

The second clause symbolically becomes (note we use *z* for the
particular since it may be different than *x*)

> ∀*z* (*D(z)* → *Q(z)*)

Combining the clauses with the conditional gives

    ∃x (D(x) ∧ ∃y (F(y,x) ∧ M(y))) → ∀z (D(z) → Q(z))

**Example 6**

    ∃x (D(x) ∧ M(x)) → ∀y ∃z ((F(y,z) ∧ D(z)) → Q(y))
    
    D(x): "x lives in the dorm."
    F(y,x): "y is a friend of x."
    M(x): "x has the measles."
    Q(x): "x has to be quarantined."

Literal translation for the first clause gives

> "There exists a person that lives in the dorm and that person has the
> measles."

Literal translation for the second clause gives

> "For all persons there exists a person such that if the first is a
> friend of the second and the second lives in the dorm, then the first
> has to be quarantined."

Combining the two with the conditional and simplifying gives

    If anyone that lives in the dorm has the measles, 
    then everyone that has a friend in the dorm will have to be quarantined.
