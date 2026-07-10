---
layout: default
title: "Lecture 21: Permutations"
---

Distinct Symbol Arrangements
============================

> **Definition**
	
> For *n* *distinct* objects, the number of unique arrangements where *order matters* is known as a *permutation*.
	
> The number of permutations for *n* distinct objects is *n*!, i.e. *n* factorial defined as
	
> *n*! = *n* · *(n-1)* · ... · 2 · 1

> where *0*! = 1
		
In general, the number of permutations for *r* objects drawn from a set of *n* is given by
	
> <sub>n</sub>*P*<sub>r</sub> = *n*! \ (*n* - *r*)!
	
**Example 1**

> How many different ways can 5 people be in a line?
	
Using the multiplication rule, the first position has five possibilities, the second position has 4, etc. giving

> 5 · 4 · 3 · 2 · 1 = 5 ! = 120
	
This result is the same as <sub>5</sub>*P*<sub>5</sub>, thus we can see that permutations occur as a special case of the multiplication rule.

**Example 2**

> Suppose there are 10 people entered in a contest that awards 3 places (thus order matters). How many possible ways can the awards be given?
	
By the multiplication rule, there are 10 possibilities for 1st place, 9 for 2nd, and 8 for 3rd giving

> 10 · 9 · 8 = 720
	
Alternatively we can use permutations by noting that there are 10! total possible permutations for all 10 people, but for any set of 3 there are 7! ways to arrange the remaining people. Thus there are

> <sub>10</sub>*P*<sub>3</sub> = 10! / (10 - 3)! =  10! / 7! = 720 

**Example 3**

> A family has 6 people to be seated around a round table for Thanksgiving dinner. If rotations are ignored, how many arrangements of people are there?
	
At first we might suspect that there are 6! arrangements, however this would duplicate count rotation arrangements. Instead we simply assume the first person sits in a spot (since rotations are ignored, the particular seat is irrelevant) and then there are 

> 5! = 120 arrangements for the other people.

**Example 4**

> How many words (meaning arrangements of letters) can be made from 
	
> **COMPUTER**

Since there are 8 *distinct* letters, there would be 

> 8! = 40,320 arrangments of all 8 letters.
	
**Example 5**

> How many words (meaning arrangements of letters) can be made from 
	
> **COMPUTER**
		
> *if* **COMP** must remain together?

To solve this problem, we will treat **COMP** as a single symbol (since it must remain together) and then note that it can *only* be placed in one of the first 5 slots. Then the remaining 4 letters can be permuted into the other slots, so by the multiplication rule the total number of arrangements is

> 5 · 4! = 5 · 24 = 120
	
**Example 6**

> How many words (meaning arrangements of letters) can be made from 
	
> **COMPUTER**
		
> *if* they must *begin* with **C** and *end* with **R**?

For this variant, since the first letter *must* be **C** there are no options for that slot and similarly for the last slot which *must* be **R**. Therefore since the other letters can be in any order in the remaining 6 slots, the total number of arrangements that begin with **C** and end with **R** is

> 6! = 720

Repeated Symbol Arrangements
============================

> **Definition**
	
> For *n* objects of which there are *i* distinct sets with *k*<sub>i</sub> objects per set, i.e.
	
> *k*<sub>1</sub> + *k*<sub>2</sub> + ... + *k*<sub>i</sub> = *n*
	
The number of *unique* permutations is
	
> *n*! / (*k*<sub>1</sub>! · *k*<sub>2</sub>! · ... · *k*<sub>i</sub>!)

**Example 7**

> How many words (meaning arrangements of letters) can be made from 
	
> **MISSISSIPPI**

Initially we might say 11!, but this would overcount words where the **S**'s (and other letters that are indistinguishable) are simply rearranged but produce the same final arrangement. However we can see that there are 4! ways the **S**'s can be arranged (and 4! for **I**'s, 2! for **P**'s, and 1! for **M**'s) giving

> 11! / (4! · 4! · 2! · 1!) = 11 · 10 · 9 · 7 · 5 = 34,650

