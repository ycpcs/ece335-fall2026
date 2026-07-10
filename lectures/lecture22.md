---
layout: default
title: "Lecture 22: Combinations"
---

Combinations Without Repeats
============================

> **Definition**
	
> For *n* *distinct* objects, the number of unique arrangements of *r* objects where *order does not matter* **and** no objects are repeated is known as a *combination* (read *n* choose *r*). The number of combinations for *r* objects drawn from a set of *n* without repeats is given by
	
> <sub>n</sub>*C*<sub>r</sub> = *n*! / ((*n* - *r*)! · *r*!)
		
Note that 
	
> <sub>n</sub>*C*<sub>n-r</sub> = *n*! / (*r*! · (*n* - *r*)!)
		
and thus
	
> <sub>n</sub>*C*<sub>r</sub> = <sub>n</sub>*C*<sub>n-r</sub>
		
**Example 1**

> If a pizza shop has 10 possible toppings, how many different 3 topping pizzas can they make (assuming no repeated toppings)?
	
Since we are choosing 3 toppings from 10,

> <sub>10</sub>*C*<sub>3</sub> = 10! / (7! · 3!) = 10! / 4! = 120
	
**Example 2**

> If a pizza shop has 10 possible toppings, how many different pizzas with no more than 3 toppings can they make (assuming no repeated toppings)?
	
Now we must use the addition rule for 0, 1, 2, and 3 topping pizzas. Thus

> \# no toppings: <sub>10</sub>*C*<sub>0</sub> = 10! / (10! · 0!) = 10! / 10! = 1

> \# one topping: <sub>10</sub>*C*<sub>1</sub> = 10! / (9! · 1!) = 10! / 9! = 10

> \# two toppings: <sub>10</sub>*C*<sub>2</sub> = 10! / (8! · 2!) = 45

> \# three toppings: <sub>10</sub>*C*<sub>3</sub> = 10! / (7! · 3!) = 120
	
Therefore the total number is 1 + 10 + 45 + 120 = 176.

**Example 3**

> How many different 5 card poker hands are there from a standard 52 card deck?
	
Initially we might guess <sub>52</sub>*P*<sub>5</sub> but then we are counting hands with the same cards but in a different order multiple times. Thus the problem involves a *combination* rather than a *permutation*. Hence

> <sub>52</sub>*C*<sub>5</sub> = 52! / (47! · 5!) = 2,598,960

**Example 4**

> How many 5 card poker hands are full houses, i.e. a hand with 3-of-a-kind and a pair?
	
First we note that order does not matter and thus we will use combinations. However rather than selecting individual cards, we will approach the problem by considering the 3-of-a-kind and the pair separately.

*3-of-a-kind*

First we will pick the value of the 3-of-a-kind which is choosing 1 from 13.
	
> <sub>13</sub>*C*<sub>1</sub> = 13! / (12! · 1!) = 13
	
Next choose the 3 suits from the 4 total for the three cards giving

> <sub>4</sub>*C*<sub>3</sub> = 4! / (1! · 3!) = 4
		
Since these two choices are independent, the total number of ways is given by the multiplication rule as
	
> 13 · 4 = 52
		
*Pair*

For the pair again we first select the value but note that it *cannot* be the same as the 3-of-a-kind value. Thus there are only 12 to choose from giving
	
> <sub>12</sub>*C*<sub>1</sub> = 12! / (11! · 1!) = 12
			
Now we select the two suits from 4 giving
	
> <sub>4</sub>*C*<sub>2</sub> = 4! / (2! · 2!) = 6
		
Again since the choices are independent the total number of ways to form the pair is given by the multiplication rule as
	
> 12 · 6 = 72
		
Then combining the possible 3-of-a-kinds with the possible (different value) pairs by the multiplication rule gives

> (<sub>13</sub>*C*<sub>1</sub>)(<sub>4</sub>*C*<sub>3</sub>)(<sub>12</sub>*C*<sub>1</sub>)(<sub>4</sub>*C*<sub>2</sub>) = 52 · 72 = 3744
	
Note that we would get the same answer if we selected the pair first (which should be the case since order doesn't mattter).

Using the total number of poker hands from example 3, we see that the probability of getting a full house is

> 3744 / 2598960 = 0.14%  (i.e. just slightly more than one tenth of one percent!)
		

Combinations With Repeats
=========================

> **Definition**
	
> For *n* *distinct* types, the number of unique arrangements of *r* objects where *order does not matter* and repeats are allowed is given by
	
> <sub>r+n-1</sub>*C*<sub>r</sub> = ((*r*+*n*-1)! / ((*n*-1)! · *r*!)

**Example 5**

> Suppose you are going on a trip and taking a cooler that holds 10 cans of soda and you have 4 types of soda to choose from. How many ways can the cooler be filled?
	
An initial guess might be 10! but this is incorrect since order doesn't matter. Next we might try <sub>10</sub>*C*<sub>4</sub> but again this is incorrect since there *must* be repeats. This is known as the *pigeonhole principle* which says that if you have *n* objects to be placed in *k* slots where *k* < *n* then *at least* one slot must have multiple objects. Hence we will approach the problem by representing the cans as *X*'s and the *divisions* between types as \|'s. So for example, one arrangement might be

> XXXX\|XX\|XX\|XX
	
which would represent 4 of type 1, and 2 of types 2, 3, and 4. Thus if we look at the diagram we see that for 4 types there are 3\|'s (which in general for *n* types there are *n*-1 \|'s). Therefore for *r* objects and *n*-1 \|'s there are a total of *r*+*n*-1 slots. Therefore we simply choose *r* of these slots (for the *X*'s since the remaining ones will contain the \|'s) giving the formula

> <sub>r+n-1</sub>*C*<sub>r</sub>
	
Hence for *n*=4 types and *r*=10 cans we would have

> <sub>10+4-1</sub>*C*<sub>10</sub> = <sub>13</sub>*C*<sub>10</sub> = 13! / (3! · 10!) = 286
	
Alternatively we could place the *n*-1 \|'s since

> <sub>r+n-1</sub>*C*<sub>n-1</sub> = <sub>r+n-1</sub>*C*<sub>r</sub>
	
**Example 6**

> Suppose you are going on a trip and taking a cooler that holds 10 cans of soda and you have 4 types of soda to choose from. However you have a particular favorite soda so want to have *at least* 4 cans of that type. How	many ways can the cooler be stocked.
	
Similar to the permutation problems where certain values were specified for certain locations, here we can simply place 4 *X*'s in the first 4 slots (and assume that type 1 is our favorite). Then we simply select the remaining 6 cans from *all* 4 types (since *at least* means we may choose to have additional cans of that type). Thus the problem is now reduced to choosing 6 from 4 with repeats giving

> <sub>6+4-1</sub>*C*<sub>6</sub> = <sub>9</sub>*C*<sub>6</sub> = 9! / (3! · 6!) = 84

Pascal's Triangle
=================

> There is a relationship between the *binomial coefficients*, i.e. the coefficients for the expansion of
	
> (*x* + *y*)<sup>n</sup>
		
> and combinations <sub>n</sub>*C*<sub>r</sub>. 

Furthermore, an interesting figure known as *Pascal's triangle* is given by
	
> (*x* + *y*)<sup>0</sup>             1

> (*x* + *y*)<sup>1</sup>           1   1

> (*x* + *y*)<sup>2</sup>         1   2   1	

> (*x* + *y*)<sup>3</sup>       1   3   3   1

> (*x* + *y*)<sup>4</sup>     1   4   6   4   1

> (*x* + *y*)<sup>5</sup>    1  5  10  10  5   1

> (*x* + *y*)<sup>6</sup>   1  6  15  20  15  6  1
	
where any particular value is the *sum* of the two values *above* it.
	
Also, any particular value in the (*n*+1)<sup>th</sup> row and (*r*+1)<sup>th</sup> column can be found by <sub>n</sub>*C*<sub>r</sub> giving the equivalence
	
> <sub>n+1</sub>*C*<sub>r</sub> = <sub>n</sub>*C*<sub>r-1</sub> + <sub>n</sub>*C*<sub>r</sub>	
	
**Example 7**

> How many pizzas can be made from 5 different toppings using 3 *or less*?
	
From Pascal's triangle for *n*=5 (i.e. row 6 of the triangle) we can simply add up the first 4 values giving

> 1 + 5 + 10 + 10 = 26
	
which is equivalent to

> <sub>5</sub>*C*<sub>0</sub> + <sub>5</sub>*C*<sub>1</sub> + <sub>5</sub>*C*<sub>2</sub> + <sub>5</sub>*C*<sub>3</sub> = 1 + 5 + 10 + 10 = 26
	
Additionally, if we look at the sum of the coefficients across any particular row we see that they sum up to 2<sup>n</sup>. Thus 

> ∑<sub>n</sub>*C*<sub>i</sub> = 2<sup>n</sup>
