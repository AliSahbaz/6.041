# 9/16 lecture- Conditional Probabilities

______

### General probability shit

* P(A | B) = P(A and B) / P(B)
* P(A and B) = P(B) * P(A | B)
* P(A and B) = P(A) * P(A | B)

### Baye's rule

```
P(A | B) = P(A) * P(B | A) / P(B)
```

### Tom Apostol's Example:

So you ask a class of all boys how many boys they have in their family. Why does this not represent the sample population of the United States?

The problem is that the sample population excludes families that only have girls in them.

### Random example

#### Problem space:

2n families     n families      n families
1 girl 1 boy    2 boys          2 girls

|Ω| = 8n

#### Q1

Q: randomly-selected child comes from a family that has at least one boy?

A: 3/4?

#### Q2

Q: randomly-selected child is a boy?
P(boy) = 1/2
P(girl) = 1/2

P(B | A) = P(A and B) / P(A)

A: 2/3

### Independence (stochastic independence, mutual independence)

A, B indep if P(A|B) = P(A)

Ex: Deck of 52 cards each card equally likely to be drawn.

A: draw an ace
B: draw a heart

Q: Are these two events independent?
A: Yes


### Example of how conditioning ruins independence:

#### Problem space:

A whole bunch of overlapping boxes

A and B intersect, C intersects A and C intersects B.

#### Q1

Is A,B independent conditioned on C if

```
P(A and B | C) = P(A|C) * P(B|C)
```

Conditioned on C, A & B no longer intersect, so they are conditionally dependent.

#### Q2

What if C now does not intersect with B?

They are now independent.

eol
