---
layout: default
title: "Lecture 6: Equivalences Involving Quantifiers"
---

Quantifier Equivalents
======================

> **Quantifier Negation Laws**
>
> > ¬∃*x* *P(x)* is equivalent to ∀*x* ¬*P(x)*
> >
> > ¬∀*x* *P(x)* is equivalent to ∃*x* ¬*P(x)*

**Example 1**

    Everyone dislikes a show off.

"Everyone" represents a universal quantifier (since it implies for
all) so we can rewrite the original statement as

> ∀*x* (*x* dislikes a show off)

Symbolically representing *L(x)* for "*x* likes a show off" the
logical form is

> ∀*x* (¬*L(x)*)

Using the quantifier negation law, this statement is equivalent to

> ¬∃*x* (¬¬*L(x)*)
>
> ¬∃*x* (*L(x)*)

Translating back to English gives "There does not exist a person that
likes a show off." or

    No one likes a show off.

**Example 2**

    Not everyone showed up for class today.

"Everyone" is a universal quantifier (since it implies for all) and
letting *S(x)* represent "*x* showed up for class today" the symbolic
form is

> ¬∀*x* (*S(x)*)

Applying the quantifier negation law, this statement is equivalent to

> ∃*x* (¬*S(x)*)

Translating back to English gives "There exists a person that did not
show up for class today" or

    Somebody didn't show up for class today.

Quantifier Commmutative Laws
============================

> **Quantifier Commutative Laws** (note quantifiers must be the same)
>
> > ∀*x* ∀*y* *P(x,y)* is equivalent to ∀*y* ∀*x* *P(x,y)*
> >
> > ∃*x* ∃*y* *P(x,y)* is equivalent to ∃*y* ∃*x* *P(x,y)*

**Example 3**

    Everybody honors all our soldiers on Memorial Day.

"Everybody" and "all" indicate universal quantifiers (since they
imply for all) and letting *H(x,y)* represent "*x* honors *y* on
Memorial Day" and *S(y)* represent "*y* is a soldier" the symbolic
form is

> ∀*x* ∀*y* (*S(y)* → *H(x,y)*)

Commuting the quantifiers gives

> ∀*y* ∀*x* (*S(y)* → *H(x,y)*)

Which means

    On Memorial Day, all of our soldiers are honored by everyone.

Quantifier Distributive Laws
============================

> **Universal Distributive Laws** (note only for ∀ with ∧)
>
> > ∀*x* (*P(x)* ∧ *Q(x)*) is equivalent to ∀*x* *P(x)* ∧ ∀*x* *Q(x)*
>
> **Existential Distributive Laws** (note only for ∃ with ∨)
>
> > ∃*x* (*P(x)* ∨ *Q(x)*) is equivalent to ∃*x* *P(x)* ∨ ∃*x* *Q(x)*

**Example 4**

    Someone likes vanilla or chocolate ice cream.

"Someone" indicates an existential quantifier (since it implies there
exists) and letting *V(x)* represent "*x* likes vanilla ice cream" and
*C(x)* represent "*x* likes chocolate ice cream" the symbolic form is

> ∃*x* (*V(x)* ∨ *C(x)*)

Distributing the quantifier gives

> ∃*x* *V(x)* ∨ ∃*x* *C(x)*

Which means

    There is someone likes vanilla ice cream or there is someone that likes chocolate ice cream.

(Note in this case we interpret the **or** to mean it *could* be the
same person and thus we use the same particular *x* in both clauses).

Unique Particular
=================

> **Definition**

> > For "There is a *unique* *x* such that *P(x)*", we write ∃!*x*
> > (*P(x)*).

**Unique Particular Law**

> ∃!*x* (*P(x)*) is equivalent to ∃*x* (*P(x)* ∧ ¬∃*y* (*P(y)* ∧ (*y* ≠
> *x*)))

**Example 5**

    John is only taking one class this semester.

"only taking one" indicates the unique particular (since it implies
exactly one) and letting *C(j,x)* represent "*j* is taking class *x*
this semester" the logical form is

> ∃!*x* *C(j,x)*

Applying the unique particular law gives the equivalent statement

> ∃*x* (*C(j,x)* ∧ ¬∃*y* (*C(j,y)* ∧ (*y* ≠ *x*)))

Which means (in a much more convoluted way)

    "John is taking a class and there is not a different class that John is also taking."
