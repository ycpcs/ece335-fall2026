---
layout: default
title: "Lecture 20: Combinatorics"
---

Introduction
============

> **Definition**

> *Combinatorics* is the branch of mathematics focused on *counting* without *counting*.

**Example 1**

> If two fair coins are flipped, what is the probability of getting *exactly* one head.

The possible options are to get 0, 1, or 2 heads so intuitively we would guess the probability is 1/3. However the problem with this reasoning is that each outcome is *not* equally likely. Rather we must enumerate the actual outcomes as

> TT, TH, HT, HH

which we see has *four* possiblities, two of which contain exactly one head and thus the probability is 1/2.

**Example 2**

> *Monty Hall Problem*
>
> You are presented with three doors to choose from, one of which contains a prize. After guessing one, a door *without* a prize is opened. Should you switch your guess or not?

At first glance there does not seem to be any reason why you would switch your guess, however this is incorrect. Originally your first guess has a 1/3 chance of being correct. But *after* one of the doors is opened that does not contain the prize, if we consider the two remaining doors, the one you *didn't* pick now has a 1/2 chance of being the right one.

Multiplication Rule
===================

> **Definition**

> If each choice in a sequence of selections is *independent*, then the final number of possibilities for the sequence is the *product* of the individual possibilities, i.e. the *multiplication rule*. Note this is equivalent to the number of elements in the *Cartesian Product* of the sets of individual possibilities.

**Example 3**

> Assume the digits 2-9 on a telephone are each associated with 3 letters of the alphabet. How many words are possible for 7 digit phone numbers?

Consider this problem as one where we have 7 slots and each slot can contain one of 3 possible values. Thus the total number of different words is

> 3 · 3 · 3 · 3 · 3 · 3 · 3 = 3<sup>7</sup> = 2187

Note that we allow *repeated* values.

**Example 4**

> PIN numbers on ATM machines consist of 4 digit numbers. How many possible PIN numbers are there? If you can check one PIN number every second, how long would it take on average to get the correct one?

Here we have 4 slots each with 10 possible values (the numbers 0-9) giving

> 10 · 10 · 10 · 10 = 10<sup>4</sup> = 10000

or alternatively note that the numbers go from 0000-9999 which is 10000 outcomes (formula for the number of values in a range from *a* to *b* is *b*-*a*+1). Hence if a person can check 1 per second (i.e. 60 per minute) it would take

> 10000/60 = 166.7 minutes = 2.8 hours

Assuming each outcome is equally likely (probably a poor assumption), on average only half would need to be checked giving about 1.4 hours to find the right value.

**Example 5**

> Using the same 4 digit PIN numbers as example 4, how many do not contain any repeated digits?

We still have 4 slots with the *first* one having 10 possible values. But then the *second* slot only has 9 possible values (since it cannot be the same as the first one), and the *third* slot only 8 possible values, etc. Thus the number of PIN that do not have any repeated digits is

> 10 · 9 · 8 · 7 = 5040

which is 5040/10000 = 50.4% of them.

**Example 6**

> Given a combination lock with numbers 0-39, how many possible 3 number combinations are there? If each value can be off by one, then how many combinations are there?

Since there are 40 numbers from 0-39, the total number of combinations is

> 40<sup>3</sup> = 64,000

However if each value can be off by one, i.e. 1 covers {0,1,2}, 4 covers {3,4,5}, etc. then the possible numbers are only {1, 4, 7, 10, 13, 16, 19, 22, 25, 28, 31, 34, 37, 39} which is 14 values. Thus the actual number of combinations is only

> 14<sup>3</sup> = 2744

which is only 4.3% of the supposed combinations.

**Example 7**

> Suppose there are 4 people (say *A*, *B*, *C*, *D*) to fill the officer positions of president, vice-president, treasurer, and secretary. However,

- *A* cannot be president

- *C* or *D* must be secretary

How many different ways can the positions be filled?

Since there are 3 possibilites for president, leaving 3 possibilities for vice-president, 2 for secretary, and then just 1 for treasurer the number of different ways would be

> 3 · 3 · 2 · 1 = 18  which is **WRONG!**

Unfortunately these events are *not* independent (since if *C* is selected as president and *D* is selected as vice-president then there is no one that can fill the secretary position, thus giving an infeasible outcome). However if we fill the positions in a different order to enforce the constraints we can use the multiplication rule.

First select the *secretary* of which there are two possiblities (*C* or *D*). Then choose the president of which there are two possibilities (*B* or the one not chosen for secretary). Then choose vice-president of which there are two possibilities. And finally there will only be one person left for treasurer. Thus the number of possible outcomes is

> 2 · 2 · 2 · 1 = 8

Addition Rule
=============

> **Definition**

> If the choices are *disjoint*, then the number of possibilities are *added* together, i.e. *addition rule*.

**Example 8**

> In programming languages, variable names must start with a letter and may contain only letters, numbers, and the underscore character. How many possible variable names are there with 4 or fewer characters?

Since the first character must be a letter (which can be upper or lower case), there are 52 possibilities. For all subsequent characters there are 52 (letters) + 10 (numbers) + 1 (underscore) = 63 possibilities.

To find the total number of variable names we will add up all the
variables of length 1 plus the variables of length 2, etc.

> \# variables of length 1 = 52

> \# variables of length 2 = 52 · 63 = 3276

> \# variables of length 3 = 52 · 63<sup>2</sup> = 206388

> \# variables of length 4 = 52 · 63<sup>3</sup> = 13002444

Thus the total number of possible variable names is
52+3276+206388+13002444 = 13,212,160.

Complement Rule
===============

> **Definition**

> If the number of possibilities for the *complement* of the desired set can be determined, then the desired number of possibilities can be found by *subtracting* the complement from the total number of possibilities, i.e. *complement rule*.

**Example 9**

> Using the rules for variable names from example 8, how many 4 character names contain *repeated* symbols?

From example 8 we know that there are 13,212,160 possible variables *including* ones with repeated symbols. Thus we will compute the number of variables that do *not* contain any repeated symbols (again using the addition rule).

> \# variables of length 1 (no repeats) = 52

> \# variables of length 2 (no repeats) = 52 · 62 = 3224

> \# variables of length 3 (no repeats) = 52 · 62 · 61 = 196664

> \# variables of length 4 (no repeats) = 52 · 62 · 61 · 60 = 11799840

Thus there are 52+3224+196664+11799840 = 11,999,780 variables *without* repeats. Therefore there are 13212160 - 11999780 = 1,212,380 variables that contain repeated symbols (roughly 9.2%).

**Example 10**

> How many integers between 1-100 are *not* divisible by 7?

We could find this number manually by checking every number between 1-100 to see if it is divisible by 7, or apply the complement rule by finding how many *are* divisible by 7 and subtracting from 100 (since there are 100 numbers between 1-100).

To find the number that are divisible we note that there is a correspondance between the divisible values and the integers as

> 7 = 1 · 7

> 14 = 2 · 7

> 21 = 3 · 7

> ...

> 98 = 14 · 7

Thus the number of values divisible by 7 is the *same* as the number of integers between 1-14 which is 14. (14-1+1=14).

Thus since there are 14 values that are divisible by 7, there are 100-14 = 86 that are not divisible by 7.
