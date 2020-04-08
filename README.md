# Math Structures W11

[toc]

## Structures, proofs

<u>*Defn.*</u> A structure contains define objects and ways to combine them.

<u>*Ex.*</u>

- $\mathbb{R}$, combine using +, -, *, /
- Sets, combine using union, subset ...
- Logical statements (what we will talk about today)

<u>*Defn.*</u>: Reasoning that makes use of this structure and the English language..

## Proposition

*<u>Defn.</u>* A <u>proposition</u> \\[ P \\] is a sentence that is either true or false, but not both.

*<u>Ex.</u>*

- 2 + 3 = 4, P, truth value: False
- I have two children, Q, true value: True
- “This statement is false” can’t be assigned a truth value, so it is not a proposition,

How to combine 2+ propositions to create a new one? Using <u>logical connectives</u>.

<u>*Truth table for examples.*</u>

|  P   |  Q   | P and Q, conjunction $P \and Q$ | P or Q, disjunction $P \or Q$ | not-P, negation $\lnot P$ |
| :--: | :--: | :-----------------------------: | :---------------------------: | :-----------------------: |
|  T   |  T   |                T                |               T               |             F             |
|  T   |  F   |                F                |               T               |             F             |
|  F   |  T   |                F                |               T               |             T             |
|  F   |  F   |                F                |               F               |             T             |

## Conditional

A conditional logical connective is also a way to combine propositions, in addition to the ones listed above.

*<u>Defn.</u>* A conditional logical connective $P \rightarrow Q$ says this: does a combination of P and Q contradicts if P then Q?

- P: hypothesis / antecedent
- Q: conclusion / consequence

*<u>Truth table.</u>*

|  P   |  Q   | $P \rightarrow Q$ |
| :--: | :--: | :---------------: |
|  T   |  T   |         T         |
|  T   |  F   |         F         |
|  F   |  T   |         T         |
|  F   |  F   |         T         |

<u>*Ex.*</u> Suppose P is “I kicked the ball” and Q is “the ball moved”. Then the truth table above translates to:

- Does "I kicked the ball" and "the ball moved" support the if-then? 
    - Yes.
- Does "I kicked the ball" and "the ball did not move" support the if-then? 
    - No.
- Does "I didn't kick the ball" and "the ball moved" support the if-then? 
    - Well, at least it doesn't contradict it - so yes.
    - Explanation: "Perhaps a strong gust of wind moved the ball, or a toddler came along, while you were drinking water, and kicked the ball.” ([Stackexchange Math](https://math.stackexchange.com/questions/3612615/conditional-logical-connectives-p-to-q/3612630#3612615))
- Does "I didn't kick the ball" and "the ball did not move" support the if-then? 
    - Well, at least it doesn't contradict it - so yes.

## Biconditional

A biconditional logical connective is also a way to combine propositions, in addition to the ones listed above.

*<u>Defn.</u>* A conditional logical connective $P \iff Q$ says this: does a combination of P and Q contradicts P iff Q (P happens whenever Q happens, and P fails whenever Q fails)?

*<u>Truth table.</u>*

|  P   |  Q   | $P \rightarrow Q$ |
| :--: | :--: | :---------------: |
|  T   |  T   |         T         |
|  T   |  F   |         F         |
|  F   |  T   |         F         |
|  F   |  F   |         T         |

## Conditionals expressed in English

### Necessary condition

P is a necessary condition for Q is equivalent to if Q then P. 

By <u>necessary</u>, we mean that P must be true for Q to be true, but P is true is not sufficient. To verify that “P is a necessary condition for Q” is equivalent to if Q then P, we can construct a truth table as follows:

|  Q   |  P   |                         Explanation                          | P is a neccesary condition for Q. | $Q \rightarrow P$ (reference) |
| :--: | :--: | :----------------------------------------------------------: | :-------------------------------: | ----------------------------- |
|  T   |  T   | If P is true and Q is true, this does not contradict with the definition of necessity. |                 T                 | T                             |
|  T   |  F   | If P is false and Q is true, this <u>contradicts</u> with definition of necessity. |                 F                 | F                             |
|  F   |  T   | If P is true and Q is false, this does not contradict with definition of necessity. |                 T                 | T                             |
|  F   |  F   | If P is false and Q is false, this does not contradict with definition of necessity. |                 T                 | T                             |

Since the truth values of “P is a neccesary condition for Q” are the same with those of $Q \rightarrow P$, we say that the two expressions are logically equivalent.

### Sufficient condition

P is a sufficient condition for Q is equivalent to if P then Q. 

By <u>sufficient</u>, we mean that, as long as P is true, Q is true. To verify that “P is a sufficient condition for Q” is equivalent to if P then Q, we can construct a truth table as follows:

|  P   |  Q   |                         Explanation                          | P is a neccesary condition for Q. | $P \rightarrow Q$ (reference) |
| :--: | :--: | :----------------------------------------------------------: | :-------------------------------: | ----------------------------- |
|  T   |  T   | If P is true and Q is true, this does not contradict with "P is true, Q is true”. |                 T                 | T                             |
|  T   |  F   | If P is true and Q is false, this <u>contradicts</u> with "P is true, Q is true”. |                 F                 | F                             |
|  F   |  T   | If P is false and Q is true, this does not contradict with "P is true, Q is true” - this says nothing about Q when P is false. |                 T                 | T                             |
|  F   |  F   | If P is false and Q is false, this does not contradict with "P is true, Q is true” - this says nothing about Q when P is false. |                 T                 | T                             |

Since the truth values of “P is a sufficient condition for Q” are the same with those of $P \rightarrow Q$, we say that the two expressions are logically equivalent.

### Necessary and sufficient condition (iff)

We already know that “P is a necessary condition for Q” and “P is a sufficient condition for Q” is equivalent to $Q \rightarrow P $ and $P \rightarrow Q$ respectively. Therefore, to get the truth values for both necessity and sufficiency, we only need to apply the AND connective to the truth values of $Q \rightarrow P $ and $P \rightarrow Q$ as follows:

| $Q \rightarrow P $ | $P \rightarrow Q$ | $(Q \rightarrow P) \and (P \rightarrow Q)$ |
| ------------------ | ----------------- | ------------------------------------------ |
| T                  | T                 | T                                          |
| T                  | F                 | F                                          |
| F                  | T                 | F                                          |
| F                  | F                 | T                                          |

This means that, for "if and only if P then Q”, Q is true whenever P is true and Q is false whenever P is false.

## Logical equivalence

<u>*Defn.*</u> If A and B are propositions formed from given propositions P, Q, R, S, T, ... using and, or not, conditionals and biconditionals, then A and B are <u>logically equivalent</u> if A and B have the same truth values for all possible truth values of P, Q, R, S, T, ... .

<u>*Ex*.</u> Show P is logically equivalent to $P \and P$.

|  P   | $P \and P$ |
| :--: | :--------: |
|  T   |     T      |
|  F   |     F      |

Since P and $P \and P$ have the same truth values, they are logically equivalent, $P \cong P \and P $.

## Tautology, contradition

*<u>Defn.</u>* Let define A as a proposition fromed from other propositions. A is a <u>tautology</u> if A is always true and A is a <u>contradition</u> if A is always false.

# Math Structures W12

[toc]













