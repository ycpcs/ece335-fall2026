---
layout: default
title: "Lecture 2: Deductive Reasoning and Logical Connectives"
---

Translating English to Symbols
==============================

**Example 1**

    It will either rain or snow tomorrow.
    It's too warm for snow.
    Therefore, it will rain.

*P*: "It will rain tomorrow."

*Q*: "It will snow tomorrow."

"It will either rain or snow tomorrow" ⇒ *P* ∨ *Q*.

"It\'s too warm for snow" ⇒ ¬ *Q*.

"Therefore, it will rain" ⇒ ∴ *P*.

Hence we can represent the argument symbolically as

    P ∨ Q
    ¬ Q 
    ∴ P


**Example 2**

    Either Bill is at work and Jane isn't, or Jane is at work and Bill isn't.

*B*: "Bill is at work."

*J*: "Jane is at work."

"Bill is at work and Jane isn't" ⇒ (*B* ∧ ¬*J*)

"Jane is at work and Bill isn't" ⇒ (*J* ∧ ¬*B*)

Combining gives

    (B ∧ ¬J) ∨ (J ∧ ¬B)

**Example 3**

    "You won't go skiing, or you will and there won't be any snow."

    ¬G ∨ (G ∧ ¬S)

**Example 4**

    Rain and snow are the only two possibilities for tomorrow's weather.

Equivalently, either it will rain *or* snow tomorrow. (note the *and*
semantically means *or* in the original sentence)

    R ∨ S

Translating Symbols to English
==============================

**Example 1**

    S: "John is stupid." 
    L: "John is lazy."

    ¬S ∧ (L ∨ S)

(*Not* John is stupid) *and* (John is lazy *or* John is stupid).

    John is not stupid, and John is either lazy or stupid.

**Example 2**

    P: "I will buy the pants."
    S: "I will buy the shirt."

    ¬P ∧ ¬S

(*Not* I will buy the pants) *and* (*not* I will buy the shirt).

⇒ I will not buy the pants, and I will not buy the shirt.

    I will not buy either the shirt or the pants.

(equivalently, I will buy neither the shirt nor the pants.)
