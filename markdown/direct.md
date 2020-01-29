---
title: Guide to Direct Proof
...

A direct proof works by applying a sequence of axiomatic steps to transform the hypothesis into the result. Direct proof is pervasive, being used internally within almost every other proof technique.

# Axioms

An **axiom** is something we take as true without proof. $\lnot \lnot A \equiv A$ is an example of an axiom. During proof writing, we commonly treat as axiomatic a much larger set of truths than we wold call axiomatic when designing a logic: effectively, we treat any step we expect our readers can follow and not doubt as if it were an axiom. Sometimes the larger truths used as axioms during a proof are called **proof rules**.

Direct-proof axioms are of two types:

Equivalences
:   If $\mathcal A \equiv \mathcal B$ then $\mathcal A$ is true whenever $\mathcal B$ is true and false whenever it is false.
    
    When proving new equivalences, our direct proof steps must all themselves by equivalences.
    Equivalences are commutative, so we can use them in either direction in our proof: from $\mathcal A$ to $\mathcal B$ or from $\mathcal B$ to $\mathcal A$, as whichever is helpful.
    
    Note that $\mathcal A \equiv \mathcal B$ and $\mathcal A \leftrightarrow \mathcal B \equiv \top$ are two ways of saying the same thing.
    
    Any expression that is equivalent to $\top$ is called a **tautology**.
    Any expression that is equivalent to $\bot$ is called a **contradiction**.

Entailments
:   If $\mathcal A \vDash \mathcal B$ then $\mathcal A$ being true is sufficient to establish the truth of $\mathcal B$, but not vice-versa: $\mathcal B$ could be true even when $\mathcal A$ is false.
    
    When proving entailments, we may use any mix of entailments and equivalences in our proof.
    Entailments are not commutative: we must use them in the direction indicated in our proof.
    
    Note that $\mathcal A \equiv \mathcal B$ and $\mathcal A \rightarrow \mathcal B \equiv \top$ are two ways of saying the same thing.
    
    If $\mathcal A \equiv \mathcal B$ then both $\mathcal A \vDash \mathcal B$ and $\mathcal B \vDash \mathcal A$, and vice-versa.
    
We have a [list of axioms](axioms.html) you may find helpful, and will add to it from time to time as we discuss new kinds of axioms during class.

# Strategy

Direct proofs are a bit like a puzzle:
You look at where you are, find all the pieces that could fit, and then pick one that seems most likely to help make progress.

## See where you are

At any given point in a proof, you have some things you know (are are assuming) are true.
Initially, that is just the given of the proof.
Every time you apply a proof step, you add one more thing to the set of things you know.

:::example
Prove that $P \land (P \rightarrow Q)$ is equivalent to $P \land Q$.

::: {.proof .frag}
Given $P \land (P \rightarrow Q)$,
we apply the definition of implication to get
$P \land (\lnot P \lor Q)$;
…
:::

At this point in the proof, we know two things:
$P \land (P \rightarrow Q)$ and $P \land (\lnot P \lor Q)$.
The next proof step can proceed from either part.
:::

In general, you want to proceed from the last step,
but in some cases (particularly some more complicated entailments)
you may want to have several chains you combine later on.

## See what can fit

There are only a few axioms that apply in most situations,
generally dictated by the connectives in a what you know.

You can always use double negation, and in many places, since it does not depend on anything;
you can also always add an $\lor \bot$ or an $\land \top$, though those are rarely helpful.
And there are a few axioms that can be used for each logical connective.

:::example
Prove that $P \land (P \rightarrow Q)$ is equivalent to $P \land Q$.

::: {.proof .frag}
Given $P \land (P \rightarrow Q)$,
we apply the definition of implication to get
$P \land (\lnot P \lor Q)$;
…
:::

Let's assume we're continuing from the last step: $P \land (\lnot P \lor Q)$.
We can

- double-negate the first $P$, the second $P$, the $Q$, the parenthesized $\lor$, or the entire expression
- distribute the $\land$ over the $\lor$
- apply the definition of implication to the $\lor$
:::

## Pick one that makes progress

Not all axioms are equally useful; you want to use the one that will get you closer to your goal. While not always sufficient, the following can help:

- don't undo what you've done
- turn everything to ands and ors, work with those, then change back
- De Morgan changes ands to ors and vice versa, and can be enabled by double negation
- implications come from disjunctions, possibly with a double negation to get the negated term for the antecedent

When none of these obviously apply, it's generally wise to pick a step that changes the formula a lot (such as distribution) or simplifies it.

:::example
Prove that $P \land (P \rightarrow Q)$ is equivalent to $P \land Q$.

::: {.proof .frag}
Given $P \land (P \rightarrow Q)$,
:::

We convert to ands and ors first, as we have more rules for them:

::: {.proof .cont .frag}
we apply the definition of implication to get
$P \land (\lnot P \lor Q)$;
:::

We listed options above. Of those, distribution will get us a $P \land Q$ as one term; we want it on its own, but having it as a term seems closer than not having it as a term

::: {.proof .cont .frag}
distribution gives us $(P \land \lnot P) \lor (P \land Q)$,
:::

Now we can simplify, almost always a good idea

::: {.proof .cont}
which can be simplified as $\bot \lor (P \land Q)$,
which simplifies to $P \land Q$.
:::

and that finished the proof!
Of course, many proofs are quite a bit longer,
but the same guidelines still hold.
:::