---
layout: default
title: "Lecture 7: Variables and Sets"
---

Set Enumeration
===============

> **Definition**

> > A *set* is a collection of objects known as *elements*. A set can be
> > defined by *listing* the elements between { }. We denote that an object
> >is an element of a set using the symbol ∈.

**Example 1**

    List the elements of the set of all positive even numbers less than 10.

Denoting the set by *A*, we have

    A = {2, 4, 6, 8}

**Example 2**

    Let D = {penny, nickel, dime, quarter} (i.e. the coin denominations).

    Is 30¢ ∈ D?

Since there is not a 30¢ coin in current US monetary denominations

    30¢ ∉ D

Note that even though we can make 30¢ *from* elements of the set *D*,
30¢ *itself* is not in the set.

**Example 3**

    Let P be the set of monetary amounts formed by pairs of coins.

    Is 30¢ ∈ P?

This set contains 10 elements (later we will see how to determine this
number)

> *P* = {2, 6, 10, 11, 15, 20, 26, 30, 35, 50}

Since 30¢ can be obtained with a nickel plus a quarter

    30¢ ∈ P

Note that since the set is the *amounts*, 30¢ is the set element and
*not* (nickel + quarter).

Set Definition
==============

> **Definition**

> > Alternatively, a *set* can be *defined* by providing a *rule*, known as
> > an *elementhood test*, that describes which elements are in the set
> > (particularly if the set contains an infinite number of objects). We
> > denote the set by *A* = {*x* \| \"rule describing *x*\"}

**Example 4**

    P = {x | x is a prime number}

    Is 9 ∈ P?

Since we can write 9 = 3\*3 ⇒ 9 is *not* prime and thus

    9 ∉ P

**Example 5**

    Give an elementhood test for the set

    S = {1, 4, 9, 16, 25, ...}

Note here that the *ellipsis* (i.e. "...") represents an infinite
number of elements and thus we must deduce the pattern from the existing
examples. Obviously the elements are 1 = 1<sup>2</sup>, 4 = 2<sup>2</sup>, 9 = 3<sup>2</sup>, 16 = 4<sup>2</sup>, 25 = 5<sup>2</sup>, etc. So the set contains elements that are the squares of the integers giving

    S = {x | x is the square of an integer}

Variables and Truth Sets
========================

> **Definition**

> > A *free variable* is an object of a set defined by the elementhood test.
> > A *bound variable* (or *dummy variable*) is a letter used for
> > convenience when giving an elementhood test.

**Example 6**

    Identify the variables in the statement

    y ∈ {x | x² < 9}

Note that this statement could be rewritten as

> "*y* is an element of the set of values whos square is less than 9"

Thus *y* is a *free variable* since its value will determine the truth
of the statement. However, *x* is a *bound variable* since the variable
*x* is simply used to express the elementhood test *x*<sup>2</sup> < 9.

> **Definition**

> > The *truth set* is the set of values for a statement *P(x)* for which
> > the statement is *true*. Thus

> > Truth set of *P(x)* = {*x* \| *P(x)*}


**Example 7**

    Give the truth set of the statement

    P(x) = {x | x is an even prime number}

Since the only prime number that is even is 2, the truth set is

    {2}

NOTE: The answer 2 is *incorrect* since that is only an *element* of a
set. Thus 2 ∈ {2}, but 2 ≠ {2}. Hence the truth *set* (which only
contains a single element) is {2}.

> **Definition**

> > The *empty set* is the set that contains no elements, denoted ∅ or { }.
> > Thus if *P(x)* is *false* for all values of *x*, i.e. no values pass the
> > elementhood test, then the truth set of *P(x)* = ∅.

Universe of Discourse
=====================

> **Definition**

> > The set of all possible values for a free variable is known as the
> > *universe of discourse* (or just the *universe*). The free variable is
> > said to *range over* this universe. Often the universe of discourse is
> > obvious from context, but can also be explicitly specified in the
> > elementhood test.

**Example 8**

    Determine the truth set for the statement

    P(x) = {x ∈ ℝ | x² < 9}
    
Since the universe of discourse is the real numbers, the values for
which this statement are true are any number greater than -3 and less
than 3 giving

    {x | -3 < x < 3}

**Example 9**

    Determine the truth set for the statement

    P(x) = {x ∈ ℕ | x² < 9}

Now since the universe of discourse is restricted to only the natural
numbers, the values for which this statement are true are any *integer*
greater than or equal to 0 and less than 3 giving

    {0, 1, 2}
