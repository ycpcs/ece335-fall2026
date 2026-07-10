---
layout: default
title: "Lecture 11: Proofs Involving Negations and Conditionals"
---

Negation Restatement
====================

### Negated Proof Template

> To prove a *negated* statement, rewrite a logically equivalent
> *positive* statement for the goal. Then apply an appropriate proof
> strategy to show the logically equivalent goal.

> The form of the formal proof will have the form:

> Suppose *P*. Then ¬*Q*.

> > \[Proof of equivalence for ¬*Q* goes here.\]

> Therefore, ¬*Q*.

**Example 1**

> Suppose *A* ∩ *C* ⊆ *B* and *a* ∈ *C*. Prove that *a* ∉ (*A* \\ *B*).

First we identify the original givens and goals

> *Givens*
>
> > *A* ∩ *C* ⊆ *B*
> >
> > *a* ∈ *C*
>
> *Goal*
>
> > *a* ∉ (*A* \\ *B*)

Examining the logical form of the goal we have

> ¬(*a* ∈ *A* ∧ *a* ∉ *B*)

Which by DeMorgan\'s law is equivalent to

> (*a* ∉ *A* ∨ *a* ∈ *B*)

and by the conditional law can be rewritten as

> *a* ∈ *A* → *a* ∈ *B*

Thus our givens and goals are equivalent to

> *Givens*
>
> > *A* ∩ *C* ⊆ *B*
> >
> > *a* ∈ *C*
>
> *Goal*
>
> > *a* ∈ *A* → *a* ∈ *B*

However now the goal is in the form of a conditional, so we can assume
the first part as a given leaving only the last part as the goal (which
is a positive statement)

> *Givens*
>
> > *A* ∩ *C* ⊆ *B*
> >
> > *a* ∈ *C*
> >
> > *a* ∈ *A*
>
> *Goal*
>
> > *a* ∈ *B*

Now we can examine the first given\'s logical form as

> ∀ *x* (*x* ∈ *A* ∩ *C* → *x* ∈ *B*)

> ∀ *x* ((*x* ∈ *A* ∧ *x* ∈ *C*) → *x* ∈ *B*)

From this statement we can deduce that from the other two givens, since
*a* ∈ *C* and *a* ∈ *A* that *a* ∈ (*A* ∩ *C*) and thus *a* ∈ *B* which
is the new goal.

Thus the formal proof would be

> **Theorem.** Suppose *A* ∩ *C* ⊆ *B* and *a* ∈ *C*. Then *a* ∉ (*A* \\ *B*).
>
> *Proof.* 
> > Suppose *a* ∈ *A*. Since *a* ∈ *C* we have *a* ∈ (*A* ∩ *C*)
> > and because *A* ∩ *C* ⊆ *B* implies that *a* ∈ *B*. However,
> > since *a* ∈ *B* it cannot be in (*A* \\ *B*).
> > 

> Therefore, *a* ∉ (*A* \\ *B*).

Proof By Contradiction
======================

### Proof By Contradiction Template

> Alternatively, to prove a *negated* statement, .i.e. ¬*P*, *assume* that the
> non-negated statement *P* as a given and derive a *contradiction* as the
> goal (usually with one of the other givens). Therefore since the
> contradiction means the assumption is invalid, the original negated
> statement must be true. One technique in reaching a contradiction is
> that if any of the original givens are negated, to select the goal to be
> the non-negated given (thus forming a contradiction).

> The form of the formal proof will have the form:

> Suppose not, and assume *P* is true.

> > \[Proof leading to contradiction goes here.\]

> Therefore, ¬*P*.

**Example 2**

> Suppose *A* ⊆ *B*, *a* ∈ *A*, and *a* ∉ *B* \\ *C*. Prove that *a* ∈
> *C*.

Identifying the original givens and goals

> *Given*
>
> > *A* ⊆ *B*
> >
> > *a* ∈ *A*
> >
> > *a* ∉ *B* \\ *C*
>
> *Goal*
>
> > *a* ∈ *C*

We will attempt a proof by contradiction by assuming *a* ∉ *C* and
deriving a contradiction. Thus the givens and goals become

> *Given*
>
> > *A* ⊆ *B*
> >
> > *a* ∈ *A*
> >
> > *a* ∉ *B* \\ *C*
> >
> > *a* ∉ *C*
>
> *Goal*
>
> > *contradiction*

Since *A* ⊆ *B* and *a* ∈ *A* implies that *a* ∈ *B*. But since *a* ∉
*C* means that *a* ∈ *B* \\ *C* which contradicts the third given. Thus
the assumption is incorrect and *a* ∈ *C*.

Thus the formal proof would be

> **Theorem.** Suppose *A* ⊆ *B*, *a* ∈ *A*, and *a* ∉ *B* \\ *C*.
> Then *a* ∈ *C*.
>
> *Proof.* 
> Suppose not, and assume *a* ∉ *C*. 
> > Since *A* ⊆ *B* and *a* ∈ *A* we have *a* ∈ *B*. 
> > However, *a* ∉ *C* means that *a* ∈ *B* \\ *C*
> > which contradicts that *a* ∉ *B* \\ *C*. 
> > 

> Therefore *a* ∈ *C*.

Modus Ponens
============

### Proof By Modus Ponens Template

> Given a statement in the form *P* → *Q*, if it can be proven that *P* is
> true, then it can be concluded that *Q* is true. This type of valid
> argument is known as *modus ponens* (meaning \"affirm by affirming\").
>
> The form of the formal proof will have the form:

> Suppose *P* → *Q*.

> > \[Proof of *P* goes here.\]

> Therefore, *Q*.

**Example 3**

> Suppose *A* ⊆ *B*, *a* ∈ *A*, and *a* ∉ *B* \\ *C*. Prove that *a* ∈
*C*.

Identifying the original givens and goals

> *Given*
>
> > *A* ⊆ *B*
> >
> > *a* ∈ *A*
> >
> > *a* ∉ *B* \\ *C*
>
> *Goal*
>
> > *a* ∈ *C*

Using the definition of set difference for the third given gives

> ¬(*a* ∈ *B* ∧ *a* ∉ *C*)

By DeMorgan\'s law

> *a* ∉ *B* ∨ *a* ∈ *C*

Then rewritting using a conditional, this given becomes

> *a* ∈ *B* → *a* ∈ *C*

Therefore we can rewrite our givens and goals as

> *Given*
>
> > *A* ⊆ *B*
> >
> > *a* ∈ *A*
> >
> > *a* ∈ *B* → *a* ∈ *C*
>
> *Goal*
>
> > *a* ∈ *C*

Since the new third given is a conditional that implies the goal, by
modus ponens if we can show *a* ∈ *B* we will have proven *a* ∈ *C*.
Thus we can convert our goal to *a* ∈ *B* (of course removing the third
given from the list) giving

> *Given*
>
> > *A* ⊆ *B*
> >
> > *a* ∈ *A*
>
> *Goal*
>
> > *a* ∈ *B*

Now the proof becomes straight forward since given that *A* ⊆ *B* and
*a* ∈ *A* implies that *a* ∈ *B*.

Thus the formal proof would be

> **Theorem.** Suppose *A* ⊆ *B*, *a* ∈ *A*, and *a* ∉ *B* \\ *C*.
> Then *a* ∈ *C*.
>
> *Proof.*
> > Since *a* ∈ *A* and *A* ⊆ *B* means that *a* ∈ *B*.
> > But because *a* ∉ *B* \\ *C* it follows that *a* ∈ *C*.

> Therefore, *a* ∈ *C*.

Note this theorem is the same as Example 2 but was derived an
alternative way.

Modus Tollens
=============

### Proof By Modus Tollens Template

> Given a statement in the form *P* → *Q*, which by contrapositive is
> equivalent to ¬*Q* → ¬*P*, if it can be proven that ¬*Q* is true (i.e.
> that *Q* is false), then it can be concluded that ¬*P* is true (i.e.
> that *P* is false). This type of valid argument is known as *modus
> tollens* (meaning \"denies by denying\").

> The form of the formal proof will have the form:

> Suppose *P* → *Q*.

> > \[Proof of ¬*Q* goes here.\]

> Therefore, ¬*P*.

**Example 4**

> Suppose *P* → *Q* and *R* → ¬*Q*. Prove that *P* → ¬*R*.

Writing the original givens and goals

> *Givens*
>
> > *P* → *Q*
> >
> > *R* → ¬*Q*
>
> *Goal*
>
> > *P* → ¬*R*

Since the goal is in the form of a conditional, we can assume the left
hand side and make the goal simply the right

> *Givens*
>
> > *P* → *Q*
> >
> > *R* → ¬*Q*
> >
> > *P*
>
> *Goal*
>
> > ¬*R*

Using the first and third givens, by modus ponens we conclude *Q* which
is now a new given

> *Givens*
>
> > *R* → ¬*Q*
> >
> > *Q*
>
> *Goal*
>
> > ¬*R*

By rewriting the new second given as

> *Givens*
>
> > *R* → ¬*Q*
> >
> > ¬(¬*Q*)
>
> *Goal*
>
> > ¬*R*

we see that a given is the negation of the right hand side of an
implication. Thus by modus tollens the negation of the left hand side is
true, i.e. ¬*R* which is the goal.

Thus the formal proof would be

> **Theorem.** Suppose *P* → *Q* and *R* → ¬*Q*. Then *P* → ¬*R*.
>
> *Proof.* 
> > Suppose *P*, then since *P* → *Q*, it follows that *Q*. 
> > Since *R* → ¬*Q*, but *Q* gives ¬*R*.
> >

> Therefore, *P* → ¬*R*.
