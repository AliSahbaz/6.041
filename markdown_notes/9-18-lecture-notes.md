# 9/18/13 lecture
* Pairwise & Mutual Independence
* Counting

______

## Mutual Independence:

Recall that A, B independent, P(A and B) = P(A) * P(B)
Mutual is when:
```
P(A and B and C) = P(A) * P(B) * P(C)
```
Mutual implies pairwise, but pairwise does not imply mutual

A, B, C are indep. if
```
P(A and B) = P(A) * P(B)
P(B and C) = P(B) * P(C)
P(A and C) = P(A)P(C)
AND
P(A and B and C) = P(A) * P(B) * P(C)
```

### Example

```
Omega = {a,b,c,abc}

A = {a,abc}
B = {b,abc}
C = {c,abc}
```

Each of the tickets is equally likely to be selected. What is P(A)?

1. Establish that A, B, and C are pairwise independent
2. Show that P(A and B and C) != P(A) * P(B) * P(C)

```
P(A) = 1/2
P(B) = 1/2
P(C) = 1/2

All intersections = {abc}
P(A and B) = 1/4
P(A and C) = 1/4
P(B and C) = 1/4

Total intersection = {abc}
P(A and B and C) = 1/4
```

1/4 != 1/2 * 1/2 * 1/2, so they are not mutually independent.
However, P(A and B) = P(A) * P(B) and so on, so they are pairwise independent.

______

## What the fuck is this

Mutual Independence of A1, A2 ... An sets

A1, ... Am if
P(Intersection of Ak) | k in S = Productsum(P(Ak))

S is an element of the Powerset({1, 2, ...n})

A **powerset** is the set of all sets of n sets
Basically, all possible combinations of subsets.
{Empty Set, {1},{2},...{n}, {1,2}, {1,3}...{n,n}, up to {n,n,.....n}}

______

## Counting

### Discrete uniform probability law

All sample points equally likely

Omega has a bunch of dots in it, with a circle A containing some of them.

|Omega| = n
|A| = n_a
P(A) = n_a/n

### Combinatorial Analysis

#### Fundamental Principle of Counting

A random experiment consists of a sequence of r subexperiments:

```
n1, n2, n3, ... nr
Omega = Omega_1 * Omega_2 * ... Omega_r

|Omega_k| = n_k
|Omega| = n1, n2 ... nr
```

#### Example
Flip a coin, then roll a 6 sided die
```
n_1=2, n_2=6 --> n = n1 * n2 = 12
```

#### Example
License plates
3 letters and 4 digits. How many possible choices?
```
26 * 26 * 26 * 10 * 10 * 10 * 10
```

#### Example
What about with distinct digits and letters?
```
26 * 25 * 24 * 23 * 10 * 9 * 8 * 7
```

#### Example
What about how many license plates with 3 letters and 4 digits?
__Haven't learned this stuff yet!__

#### Example
```
A = {a, ... a_n}
P(A) = set of all subsets of A
|P(A)|?
Answer: 2^n
```

n subexperiments, one for each element of A
each subexperiment has two outcomes

* choose for the subset
* not choose it

## Permutations

Sample space of n elements. Put them in n ranked bins.
How many ways are there to do it?
n subexperiments.

n choices * n-1 choices * n-2 choices .... 1 choice

number of ways we can order n elements is n! = n(n-1)(n-2)...(2)(1) = n factorial
verb is __permute__

#### Example

Roll a six side die six times
P(All rolls produce a distinct number)

```
6/6 * 5/6 * 4/6 * 3/6 * 2/6 * 1/6 = .015432099
6! / 6^6
```

## Combinations

If you have universal set size n, choose k elements.

How many ways?

Take the permutation * the number of possible orders
