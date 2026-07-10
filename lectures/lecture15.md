---
layout: default
title: "Lecture 15: Proof by Induction"
---

Induction Goals
===============

> To prove a goal of the form ∀*n* ∈ ℕ *P(n)* where ℕ is the set of
> natural numbers, i.e. ℕ = {0,1,2,3,\...}, first prove *P(0)*, known as
> the *base case*, and then prove ∀*n* ∈ ℕ (*P(n)* → *P(n+1)*), known as
> the *induction step*. Thus we show that the statement is true for some
> *initial value* (typically 0) and then prove that if *P(n)* is true then
> *P(n+1)* is true. Thus since *P(0)* gives *P(1)* which gives *P(2)* and
> so on proving *P(n)* for all *n*.

> The form of the formal proof will have the form:

> *Base Case.*
 
> > \[Proof of *P(0)* goes here.\] 

> *Induction Step.*
 
> > \[Proof of ∀*n* ∈ ℕ (*P(n)* → *P(n+1)*) goes here.\]

Hence, proofs by induction can be written as 6 steps:

{:start="0"}
0. Write the induction given closed form for *n*.
1. Write the induction goal closed form for *n+1* (simply substitute *n+1* for *n* in the given from step 0)
2. Show the induction given is true for a base case, typically *n* = 0.
3. Factor the induction formula for *n+1* from step 1 to include the induction formula for *n* from step 0.
4. We will **assume** the induction formula from step 0 is true, i.e. we will use the conditional proof technique from [lecture 10](lecture10.html), and substitute the closed form solution from step 0 into step 3. 
5. Perform any necessary algebra to achieve the closed form solution from step 1 for *n+1*.

**Example 1**

> Prove that for every natural number *n*, 2<sup>0</sup> + 2<sup>1</sup> + \... + 2<sup>n</sup> = 2<sup>n+1</sup> - 1.

*Step 0:* Write the induction given closed form for *n*

> ∑2<sup>i</sup> = 2<sup>n+1</sup> -1

*Step 1:* Write the induction goal closed form for *n*+1

> Substituting *n*+1 for *n* in step 1 gives

> 2<sup>0</sup> + 2<sup>1</sup> + \... + 2<sup>n</sup> + 2<sup>n+1</sup> = 2<sup>n+2</sup> - 1.

*Step 2:* Show the induction given is true for a base case.

> First we can easily show the base case for *n* = 0 since

> 2<sup>0</sup> = 1 and 2<sup>1</sup> - 1 = 2 - 1 = 1.

*Step 3* We see that the induction given in step 0 is simply the first *n* terms of the induction goal in step 1, thus

> 2<sup>0</sup> + 2<sup>1</sup> + \... + 2<sup>n</sup> + 2<sup>n+1</sup> = (2<sup>0</sup> + 2<sup>1</sup> + \... + 2<sup>n</sup>) + 2<sup>n+1</sup> = ∑2<sup>i</sup> + 2<sup>n+1</sup>

*Step 4:* Assume the induction formula from step 0 is true and substitute the closed form solution into step 3.

> Therefore we *assume* ∑2<sup>i</sup> = 2<sup>n+1</sup> - 1 is true, thus substituting gives

> ∑2<sup>i</sup> + 2<sup>n+1</sup> = (2<sup>n+1</sup> - 1) + 2<sup>n+1</sup>

*Step 5:* Perform any necessary algebra to show the closed form solution from step 1 for *n*+1

> (2<sup>n+1</sup> - 1) + 2<sup>n+1</sup> = 2 ⋅ 2<sup>n+1</sup> - 1
> > = 2<sup>n+2</sup> - 1

Thus we have proved the induction step.

Formally,

> **Theorem.** *Prove that for every natural number n*, 2<sup>0</sup> + 2<sup>1</sup> +
> \... + 2<sup>n</sup> = 2<sup>n+1</sup> - 1.
>
> *Proof.* Using induction:
>
> > *Base Case:* Letting *n* = 0, we get 2<sup>0</sup> = 1 = 2<sup>1</sup> - 1.
>
> > *Induction Step:* Let *n* be an arbitrary natural number and assume
> > that 2<sup>0</sup> + 2<sup>1</sup> + \... + 2<sup>n</sup> = 2<sup>n+1</sup> - 1. Then
> >
> > > (2<sup>0</sup> + 2<sup>1</sup> + \... + 2<sup>n</sup>) + 2<sup>n+1</sup> = (2<sup>n+1</sup> - 1) + 2<sup>n+1</sup>
> > >
> > > > = 2 ⋅ 2<sup>n+1</sup> - 1
> > > >
> > > > = 2<sup>n+2</sup> - 1

**Example 2**

> Prove that for all *n* ∈ ℕ, 0 + 1 + 2 + \... + *n* = *n*(*n* + 1)/2.

*Step 0:* Write the induction given closed form for *n*

> 0 + 1 + 2 + \... + *n* = ∑i = *n*(*n* + 1)/2

*Step 1:* Write the induction goal closed form for *n*+1

> Substituting *n*+1 for *n* in step 1 gives

> 0 + 1 + 2 + \... + *n* + (*n* + 1) = (*n* + 1)((*n*+1)+1)/2 = (*n*+1)(*n*+2)/2

*Step 2:* Show the induction given is true for a base case.

> The base case for *n* = 0 gives ∑i = 0 and 0(1)/2 = 0.

*Step 3:* We see that the induction given in step 0 is simply the first *n* terms of the induction goal in step 1, thus

> 0 + 1 + 2 + \... + *n* + *n* + 1 = (0 + 1 + 2 + \... + *n*) + (*n* + 1) = ∑i + (*n* + 1)

*Step 4:*  Assume the induction formula from step 0 is true and substitute the closed form solution into step 3.

> Therefore we *assume* ∑i = *n*(*n* + 1)/2 is true, thus substituting gives

> ∑i + (*n* + 1) = *n*(*n* + 1)/2 + (*n* + 1)

*Step 5:* Perform any necessary algebra to show the closed form solution from step 2 for *n*+1

> ∑i + (*n* + 1) = *n*(*n* + 1)/2 + (*n* + 1)
> > = (*n* + 1)(*n*/2 + 1)
> >
> > = (*n* + 1)(*n* + 2)/2

Formally,

> **Theorem.** *Prove that for all n* ∈ ℕ, 0 + 1 + 2 + \... + *n* =
> *n*(*n* + 1)/2.
>
> *Proof.* Using induction:
>
> *Base Case:* Letting *n* = 0, we get 0(1)/2 = 0.
>
> *Induction Step:* Let *n* be an arbitrary natural number and assume
> that 0 + 1 + 2 + \... + *n* = *n*(*n* + 1)/2. Then
>
> > > 0 + 1 + 2 + \... + *n* + (*n* + 1) = (0 + 1 + 2 + \... + *n*) + (*n* + 1)
> > >
> > > > = *n*(*n* + 1)/2 + (*n* + 1)
> > > > 
> > > > = (*n* + 1)(*n*/2 + 1)
> > > > 
> > > > = (*n* + 1)(*n* + 2)/2

**Example 3**

> Prove that for sufficiently large *n*, that 2<sup>n</sup> \> *n*<sup>2</sup>.

*Step 0:* Write the induction given closed form for *n*

> For sufficiently large *n*, 2<sup>n</sup> \> *n*<sup>2</sup>

*Step 1:* Write the induction goal closed form for *n*+1

> 2<sup>n+1</sup> \> (*n*+1)<sup>2</sup>

*Step 2:* Show the induction given is true for a base case.

> Here we *cannot* use *n* = 0 even though for *n* = 0, 2<sup>0</sup> = 1 > 0<sup>2</sup> = 0 and for *n* = 1, 2<sup>1</sup> = 2 > 1<sup>2</sup> = 1 because for *n* =
2, 2<sup>2</sup> = 4 = 2<sup>2</sup> and for *n* = 3, 2<sup>3</sup> = 8 < 3<sup>2</sup> = 9. Furthermore for *n* = 4, 2<sup>4</sup> = 16 = 4<sup>2</sup>.
However for *n* = 5, 2<sup>5</sup> = 32 > 5<sup>2</sup> = 25. Thus while the theorem is *not* true *for all* *n* ∈ ℕ, it may be true for *n* ≥ 5.

*Step 3:* We see that the induction goal can be factored to include the induction given, thus

> 2<sup>n+1</sup> = 2 ⋅ 2<sup>n</sup>

*Step 4:*  Assume the induction formula from step 0 is true and substitute the closed form solution into step 3.

> Therefore we *assume* 2<sup>n</sup> \> *n*<sup>2</sup> is true, thus substituting gives

> 2 ⋅ 2<sup>n</sup> \> 2 ⋅ *n*<sup>2<sup>

*Step 5:* Perform any necessary algebra to show the closed form solution from step 1 for *n*+1

> At this point we now need to show 2 ⋅ *n*<sup>2</sup> \> (*n*+1)<sup>2</sup> 

> We can expand the right hand side as (*n*+1)<sup>2</sup> = *n*<sup>2</sup> + 2*n* + 1, giving

> 2 ⋅ *n*<sup>2</sup> \> *n*<sup>2</sup> + 2*n* + 1

> Bringing *n*<sup>2</sup> from the right hand side of the
inequality to the left reduces the proof to showing for *n* ≥ 5 that

> *n*<sup>2</sup> \> 2*n* + 1

> Now we observe that for *n* ≥ 5 it is clear that *n*<sup>2</sup> = (*n*)(*n*) ≥
5*n* and thus

> *n*<sup>2</sup> ≥ 5*n*
>
> > = 2*n* + 3*n*
> > 
> > \> 2*n* + 1

Hence the theorem is true for \"sufficiently large\" *n* which in this
case is *n* ≥ 5.

Formally,

> **Theorem.** *Prove that for sufficiently large n, that 2*<sup>n</sup> \>
> *n*<sup>2</sup>.
>
> *Proof.* Using induction:
>
> *Base Case:* Letting *n* = 5, clearly 2<sup>n</sup> = 2<sup>5</sup> = 32 \> *n*<sup>2</sup> = 5<sup>2</sup> = 25. Thus 2<sup>n</sup> \> *n*<sup>2</sup> for *n* = 5.
>
> *Induction Step:* Let *n* be an arbitrary natural number greater than
> 5 and assume that 2<sup>n</sup> \> *n*<sup>2</sup>. Since *n* \> 5, clearly *n*<sup>2</sup> = (*n*)(*n*) \> 5*n*. Thus
>
> > 2<sup>n+1</sup> = 2 ⋅ 2<sup>n</sup>
> >
> > > \> 2 ⋅ (*n*<sup>2</sup>)
> > >
> > > = *n*<sup>2</sup> + *n*<sup>2</sup>
> > >
> > > ≥ *n*<sup>2</sup> + 5*n*
> > >
> > > = *n*<sup>2</sup> + 2*n* + 3*n*
> > >
> > > \> *n*<sup>2</sup> + 2*n* + 1
> > >
> > > = (*n* + 1)<sup>2</sup>

> Therefore 2<sup>n+1</sup> \> (*n* + 1)<sup>2</sup> and hence 2<sup>n</sup> \> *n*<sup>2</sup> for *n* ≥ 5.
