---
layout: default
title: "Lecture 19: Function Properties"
---

One-to-One
==========

> **Definition**

> Suppose *f*: *A* → *B*. Then *f* is known as *one-to-one* (or an
*injection*) if

> ¬∃*a*<sub>1</sub> ∈ *A* ∃*a*<sub>2</sub> ∈ *A* (*f(a*<sub>1</sub>*)* = *f(a*<sub>2</sub>*)*) ∧ *a*<sub>1</sub> ≠ *a*<sub>2</sub>)

Intuitively a function is one-to-one if every *input* has a *different
output*, i.e. no two inputs have the same output.

**Theorem**

> *f* is *one-to-one* ↔ ∀*a*<sub>1</sub> ∈ *A* ∀*a*<sub>2</sub> ∈ *A* (*f(a*<sub>1</sub>*)* = *f(a*<sub>2</sub>*)*) → *a*<sub>1</sub> = *a*<sub>2</sub>)

> If *f* and *g* are both one-to-one, then *g* ○ *f* is also one-to-one.

**Example 1**

> Let *A* = {*a*, *b*, *c*} and *B* = {*a*, *b*} and define

> *f* = {(*a*, *b*), (*b*, *b*), (*c*, *a*)}

> Is *f* one-to-one?

Clearly *f* is **not** one-to-one since for elements *a* ∈ *A* and *b* ∈
*A* we have *f(a)* = *b* and *f(b)* = *b*. (Try drawing a picture).

**Example 2**

> Let *g* = {(*x*, *y*) ∈ ℝ × ℝ \| *y* = 2*x*}

> Is *g* one-to-one?

Intuitively the equation *y* = 2*x* is clearly one-to-one but we would
like to formally prove it. We will prove it by contradiction by assuming
there exists two values *x*<sub>1</sub> ≠ *x*<sub>2</sub> such that *g(x*<sub>1</sub>*)* = *g(x*<sub>2</sub>*)* = *y*. By the equation we have *y* = 2*x*<sub>1</sub> and *y* = 2*x*<sub>2</sub> and thus 2*x*<sub>1</sub> = 2*x*<sub>2</sub> which means *x*<sub>1</sub> = *x*<sub>2</sub> thus contradicting our assumption. Hence *g* is one-to-one.

Onto
====

> **Definition**

> Suppose *f*: *A* → *B*. Then *f* is known as *onto* (or an *surjection*)
if

> ∀*b* ∈ *B* ∃*a* ∈ *A* (*f(a)* = *b*)

Intuitively a function is onto if every *output* has an *input*, i.e.
some input maps to *every* output.

**Theorem**

> *f* is *onto* ↔ Range(*f*) = *B*

> If *f* and *g* are both onto, then *g* ○ *f* is also onto.

**Example 3**

> Let *A* = {*a*, *b*, *c*} and *B* = {*a*, *b*} and define

> *f* = {(*a*, *b*), (*b*, *b*), (*c*, *a*)}

> Is *f* onto?

We see that there are elements of *A* associated with *both* elements of
*B* and thus *f* is *onto*. Formally we would state that since *f(c) =
a* and *f(a) = b* that Range(*f*) = *B* and thus *f* is *onto*.

**Example 4**

> Let *g* = {(*x*, *y*) ∈ ℝ × ℝ \| *y* = 2*x*}

> Is *g* onto?

Intuitively the equation *y* = 2*x* is clearly onto since *y* can have
any real number with appropriate choice of *x*, i.e. the line extends to
infinity in both directions. Formally, we will prove it by simply
showing that there is a real value for *x* that gives *every* value for
*y*. Thus let *y* ∈ ℝ be arbitrary, and let *x* = *y*/2 (since *y* ∈ ℝ ⇒
*x* ∈ ℝ). Then 2(*y*/2) = *y*. Hence *g* is *onto*.

**Example 5**

> Let *h* = {(*x*, *y*) ∈ ℝ × ℝ \| *y* = *x*<sup>2</sup>}

> Is *h* one-to-one? Is *h* onto?

Clearly *h* represents the graph of a parabola that passes through the
origin so intuitively we would expect it to be neither one-to-one nor
onto. We can easily show this by counterexamples.

> *One-to-one*

> Consider *x* = 1 and *x* = -1. Then *h(1) = 1* and *h(-1) = 1* yet 1 ≠
-1. Thus *h* is **not** one-to-one.

> *Onto*

> Consider *y* = -1. There is no *real* number such that *x*<sup>2</sup> = -1, thus *h* is **not** onto.

Inverse
=======

> Let *f*: *A* → *B*. If *f* is *one-to-one* **and** *onto*, then *f* <sup>-1</sup>: *B* → *A*.

In other words, *f* <sup>-1</sup> is a function (that is also *one-to-one* and
*onto*) if and only if *f* is *one-to-one* and *onto* (known as a
*bijection*).

Furthermore, if *f*: *A* → *B* with *f* <sup>-1</sup>: *B* → *A*

> (*f* <sup>-1</sup> ○ *f*) = *i*<sub>A</sub>
>
> (*f* ○ *f* <sup>-1</sup>) = *i*<sub>B</sub>

> where *i*<sub>A</sub> is known as the *identity relation* on *A* defined as 

> *i*<sub>A</sub> = {(*x*,*y*) ∈ *A* × *A* \| *x* = *y*}

> and similarly for *i*<sub>B</sub>.

**Example 6**

> Let *g* = {(*x*, *y*) ∈ ℝ × ℝ \| *y* = 2*x*}

> Does *g* <sup>-1</sup> exist, and if so determine *g* <sup>-1</sup>?

In example 2 we showed that *g* is one-to-one, and in example 3 we
showed that *g* is onto. Therefore since *g* is both one-to-one and onto
*g* <sup>-1</sup> exists. Since the formula for *g* is that *y* = 2*x*, to find
the formula for *g* <sup>-1</sup> we simply solve for *x* giving *x* = *y*/2. Thus

> *g* <sup>-1</sup> = {(*y*, *x*) ∈ ℝ × ℝ \| *x* = *y*/2}

**Example 7**

> Let *h* = {(*x*, *y*) ∈ ℝ × ℝ \| *y* = *x*<sup>2</sup>}

> Does *h* <sup>-1</sup> exist, and if so determine *h* <sup>-1</sup>?

From example 5 we saw that *h* is **not** one-to-one or onto and thus we
can conclude that *h* <sup>-1</sup> does not exist. Suppose we restrict the
*range* of *h* to only non-negative real numbers such that

> *h* = {(*x*, *y*) ∈ ℝ × ℝ<sup>+</sup> \| *y* = *x*<sup>2</sup>}

While *h* is now onto, it is still **not** one-to-one so *h* <sup>-1</sup> does
not exist. Suppose we further restrict the *domain* to only non-negative
real numbers such that

> *h* = {(*x*, *y*) ∈ ℝ<sup>+</sup> × ℝ<sup>+</sup> \| *y* = *x*<sup>2</sup>}

Now *h* *is* one-to-one and onto and thus *h* <sup>-1</sup> exists. We can
determine the formula by solving for *x* giving *x* = √y̅ where we
interpret *x* to be the positive square root. Thus

> *h* <sup>-1</sup> = {(*y*, *x*) ∈ ℝ<sup>+</sup> × ℝ<sup>+</sup> \| *x* = √y̅}

Thus this example demonstrates that a mathematical function by itself is
neither invertible or not without consideration of the domain and range.
