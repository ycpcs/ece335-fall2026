---
layout: default
title: "Lecture 9: More Operations on Sets"
---

Indexed Sets
============

### **Definition**

> An alternative way to specify an elementhood test is using quantifiers
> with the statements for the truth values for a statement

**Example 1**

> Give an alternative logical form for the set of perfect squares.

We can denote the set of perfect squares as a set of values of the form
*n*<sup>2</sup> where *n* ∈ ℕ ⇒ *S* = {*n*<sup>2</sup> \| *n* ∈ ℕ }. However this
elementhood test means that *S* is the set of values *x* such that
*there exists* a natural number whose square is *x*, i.e.

> *S* = { *x* \| ∃ *n* ∈ ℕ (*x* = *n*<sup>2</sup>) }

Hence we see that

> *x* ∈ {*n*<sup>2</sup> \| *n* ∈ ℕ} is the same as ∃ *n* ∈ ℕ (*x* = *n*<sup>2</sup>)

### **Definition**

> An *indexed set* is a set with each element is identified by a value
> (known as the *index*) drawn from an *index set*.

**Example 2**

> Use an index set to specify the set of the first 100 prime numbers.

We will denote each prime number as *p*<sub>i</sub> where 1 ≤ *i* ≤ 100. Thus the
index set can be written as *I* = {1, 2, 3, \..., 100} = {*i* \| 1 ≤ *i*
≤ 100}. Using this index set, we can write the set of the first 100
prime numbers as

> *P* = {*p*<sub>i</sub> \| *i* ∈ *I*}

Alternatively using the quantifier notation, the set can be written as

> *P* = {*p* \| ∃ *i* ∈ *I* (*p* = *p*<sub>i</sub>)}

Note that an index *set* need not be numerical values, but can contain
any objects that we wish to use for indexing the elements.

**Example 3**

> Analyze the logical form of

> {x<sub>i</sub> \| *i* ∈ *I*} ⊆ *A*

By definition of subset, we mean that *all* elements of {*x*<sub>i</sub> \| *i* ∈
*I*} are also elements of *A*. Thus

> ∀ *x* (*x* ∈ {*x*<sub>i</sub> \| *i* ∈ *I*} → *x* ∈ *A*)

Applying the alternate quantifier form then gives

> ∀ *x* (∃ *i* ∈ *I* (*x* = *x*<sub>i</sub>) → *x* ∈ *A*)

Families of Sets and Power Sets
===============================

### **Definition**

> A set whose elements are themselves sets is known as a *family of sets*
> denoted *F*. A family of sets can also be an indexed set as
> 
> *F* = {*A*<sub>i</sub> \| *i* ∈ *I*}

**Example 4**

> Create a family of sets for the favorite music groups of each person in
> the class.

We can define the index set *D* = {*d* | *d* is a student in Discrete
Math}. Then define *M*<sub>d</sub> = {*m* \| *d* likes music group *m*}. Thus the
family of favorite music groups for the entire class would be

> *F* = {*M*<sub>d</sub> \| *d* ∈ *D*}

Note that the elements of a family are *sets* thus any particular *m* ∉
*F*.

### **Definition**

> For a given set *A*, the set of *all* subsets of *A* is called the
> *power set* of *A* denoted ℘(*A*) is defined as
>  
> ℘(*A*) = {*x* \| *x* ⊆ *A*}

It can easily be shown that the number of elements of a power set, i.e.
the number of subsets, is equal to 2<sup>n</sup> where *n* is the number of
elements of the original set.

**Example 5**

> Give the power set for *A* = { bacon, eggs, ham }

Since *A* contains three elements, the power set will contain 8 *sets*.
One way to systematically generate the power set is to simply enumerate
all 3-bit strings (one bit per element) and include the element in the
subset when the bit it true.

> 000 - { }
>
> 001 - { ham }
>
> 010 - { eggs }
>
> 011 - { eggs, ham }
>
> 100 - { bacon }
>
> 101 - { bacon, ham }
>
> 110 - { bacon, eggs }
>
> 111 - { bacon, eggs, ham }

Thus the power set for *A* = { bacon, eggs, ham } is

> ℘(*A*) = { ∅, { ham }, { eggs }, { eggs, ham }, { bacon }, { bacon,
> ham }, { bacon, eggs }, { bacon, eggs, ham } }

**Example 6**

> Analyze the logical form of

> *x* ∈ ℘(*A* ∩ *B*)

Since *x* is in the powerset of *A* ∩ *B*, this statement means that *x*
is a *subset* of *A* ∩ *B*, i.e. *x* ⊆ *A* ∩ *B*. Applying the
definition of subset gives

> ∀ *y* (*y* ∈ *x* → *y* ∈ *A* ∩ *B*)

Then by the definition of intersection we get

> ∀ *y* (*y* ∈ *x* → (*y* ∈ *A* ∧ *y* ∈ *B*))

Which intuitively means that for every value, if the value is in the
subset then it must be in both *A* and *B*.

Operations on Families of Sets
==============================

### **Definition**

> For a given family of sets *F* (*F* ≠ ∅), the *intersection of the
> family*, denoted ∩*F*, is the set of elements common to *all* sets in
> the family. Symbolically
>  
> ∩*F* = {*x* \| ∀ A ∈ *F* (*x* ∈ *A*)}
>      = {*x* \| ∀ *A* (*A* ∈ *F* → *x* ∈ *A*)}
>  
> For a given family of sets *F*, the *union of the family*, denoted ∪*F*,
> is the set of elements in *any* of the sets in the family. Symbolically
>  
> ∪*F* = {*x* \| ∃ A ∈ *F* (*x* ∈ *A*)}
>      = {*x* \| ∃ *A* (*A* ∈ *F* ∧ *x* ∈ *A*)}

Intuitively the intersection are elements that every set in the family
has as an element while the union is all the elements from all the sets.
Note that this is a *set of elements* and not a set of sets.

If the family is an indexed set, i.e. *F* = {*A*<sub>i</sub> \| *i* ∈ *I*}, then
we denote the intersection and union with a slightly different notation

> ∩*F* = ∩<sub>i∈I</sub>*A*<sub>i</sub> = {*x* \| ∀ *i* ∈ *I* (*x* ∈ *A*<sub>i</sub>)}

Likewise for union

> ∪*F* = ∪<sub>i∈I</sub>*A*<sub>i</sub> = {*x* \| ∃ *i* ∈ *I* (*x* ∈ *A*<sub>i</sub>)}

**Example 7**

> Let *F* = \{\{3, 5, 7, 12}, {5, 7, 16}, {5, 7, 12, 23\}\}

> Find ∩*F* and ∪*F*.

For ∩*F* we look at all the sets in the family and find any common
elements. In this case the elements 5 and 7 are elements of all three
sets in the family, thus

> ∩*F* = {5, 7}

For the union, we simply combine all the elements from all the sets
(removing any duplicates) to give

> ∪*F* = {3, 5, 7, 12, 16, 23}

**Example 8**

> Analyze the logical form of

> *x* ∈ ℘(∪*F*)

Note that in this problem *x* is a *subset* (since it is an element of
the powerset) of the union of the family. Thus starting with the
definition of powerset

> *x* ⊆ (∪*F*) = ∀ *y* (*y* ∈ *x* → *y* ∈ ∪*F*)

Then applying the definition of union of a family, *y* ∈ ∪*F* ⇒ ∃ A ∈
*F* (*y* ∈ *A*), gives

> ∀ *y* (*y* ∈ *x* → ∃ *A* ∈ *F* (*y* ∈ *A*))

While converting the set notation into a logical statement might seem to
make things more complicated, it can be useful in determining the truth
of the statement more easily that writing out the powerset (which
contains an exponential number of sets).

**Example 9**

> Given the following sets

> *F* = \{\{1, 2, 3}, {2, 3, 4}, {3, 4, 5\}\}

> *x* = {1, 3, 5}

> Determine if the following statement is true

> *x* ∈ ℘(∪*F*)

Using set notation we could determine that ∪*F* = {1, 2, 3, 4, 5} but
this means that ℘(∪*F*) would contain 32 subsets. However if we consider
the logical form from the previous example

> ∀ *y* (*y* ∈ *x* → ∃ *A* ∈ *F* (*y* ∈ *A*))

what this statement means is that for all the elements in *y*, *if* *y*
is in *x* then there must be *at least* one set in *F* that contains
*y*. This is much easier to check as we quickly see that 1 is in the
first set, 3 is also in the first set (as well as the second and third
but we only need to find any one that contains it), and 5 is in the
third set. Thus since all elements of *x* are in at least one set in
*F*, this statement is *true* for the example.

> *x* ∈ ℘(∪*F*)

**Example 10**

> Verify the following identity
  
> ∩<sub>i∈I</sub>(*A*<sub>i</sub> \ *B*<sub>i</sub>) = (∩<sub>i∈I</sub> *A*<sub>i</sub>) \ (∪<sub>i∈I</sub> *B*<sub>i</sub>)

> (note that this is **not** a distributive law as the last term contains
∪ rather than ∩.)

Using the definition of family intersection, we can first rewrite *x* ∈
∩<sub>i∈I</sub>(*A*<sub>i</sub> \ *B*<sub>i</sub>) as

> {*x* \| ∀ *i* ∈ *I* (*x* ∈ (*A*<sub>i</sub> \ *B*<sub>i</sub>)}

Applying the definition of set difference then gives

> {*x* \| ∀ *i* ∈ *I* (*x* ∈ *A*<sub>i</sub> ∧ *x* ∉ *B*<sub>i</sub>)}
>
> {*x* \| ∀ *i* ∈ *I* (*x* ∈ *A*<sub>i</sub> ∧ ¬(*x* ∈ *B*<sub>i</sub>))}

Now we use the logical equivalency that ∀ distributes over ∧ giving

> {*x* \| ∀ *i* ∈ *I* (*x* ∈ *A*<sub>i</sub>) ∧ ∀ *i* ∈ *I* ¬(*x* ∈ *B*<sub>i</sub>)}

Then by quantifier negation we have

> {*x* \| ∀ *i* ∈ *I* (*x* ∈ *A*<sub>i</sub>) ∧ ¬∃ *i* ∈ *I* (*x* ∈ *B*<sub>i</sub>)}

Which by the definition of family union and intersection gives

> {*x* \| *x* ∈ ∩<sub>i∈I</sub> *A*<sub>i</sub> ∧ ¬(*x* ∈ ∪<sub>i∈I</sub> *B*<sub>i</sub>)}
>
> {*x* \| *x* ∈ ∩<sub>i∈I</sub> *A*<sub>i</sub> ∧ (*x* ∉ ∪<sub>i∈I</sub> *B*<sub>i</sub>)}

Finally by the definition of set difference gives

> *x* ∈ (∩<sub>i∈I</sub> *A*<sub>i</sub>) \\ (∪<sub>i∈I</sub> *B*<sub>i</sub>)
