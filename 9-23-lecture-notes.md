# 9/23 lecture

* random variables
* probability mass functions
* examples
* expected value

______

## Random Variables

A random variable is a function that maps every point in Omega to a value

```
x_1 = X(omega_1)
```

As always, functions can map to the same value, but a single input can't map to more than 1 output

Could be...

__Discrete Random Variable__, usually use K,L,M for variable

* Omega is countable

__Continuous Random Variable__, usually use X,Y,Z for variable

* Omega is uncountable

Capital letter variable is the Random Variable (RV)
Lowercase letter is the particular value of RV K

## Probability Mass Functions

```
P_K(k) = Pr(K=k)
SUM(P_K(k) = 1)
0 < P_K(k) < 1
```

### Example

```
P_K(k) = {
  ?1 | k = a, ..., b
  ?2 | e/w (ELSEWHERE)
}

?1 = 1/(b-a+1)
?2 = 0
```

### Example

PMF of the Bernoulli RV

```
P -> `1` output
1-P -> `0` output

if P = 3/4:

P_L(l) = {
  P   | l=1
  1-P | l=0
  0   | e/w
}

Draw the lollipops shit
   o o
---|-|---- l
   0 1
```

### Example
M: # of coin flips up to and including 1st H?

P -> H
1-P -> T

Draw the fucking tree

```
P -> H_1
1-P -> T_1 -> P -> H2
           -> 1-P -> T2 -> etc
```

Get each expression
```
P_M(1) = P
P_M(2) = (1-P) * P
P_M(3) = (1-P)^2 * P

P_M(m){
  (1-P)^(m-1) * P | m >= 1
  0               | e/w
}
```

Decays exponentially, called the __Geometric PMF__

### Example
L: # of Heads in n tosses of a coin

```
n = 4

P_L(l)
P_L(1) = P * (1-P)^3 * 4
P_L(l) = P^l * (1-P)^(n-l) * nCl
```

This one is called the __Binomial PMF__

### Example
2 independent rolls of a fair 4 sided die.
K1: Outcome of 1st roll
K2: Outcome of 2nd roll

```
K = K1 + K2
```

Figure out P_K(k)

```
P_K(2) = 1 * 1/4 * 1/4
P_K(3) = 2 * 1/4 * 1/4
P_K(4) = 3 * 1/4 * 1/4
P_K(5) = 4 * 1/4 * 1/4
P_K(6) = 3 * 1/4 * 1/4
P_K(7) = 2 * 1/4 * 1/4
P_K(8) = 1 * 1/4 * 1/4
```

## Expected Value (mean)
```
E(K) = SUM_k(k * PK(k))
```

It is a __weighted sum__.
Analogous to the __center of mass__.

Remember, PMF values add up to 1. You're multiplying the value times its __frequency__, all of which add up to 1, so by adding them all up you're creating a weighted sum of all values based on how frequently they occur.

### Example
E of Bernoulli RV

```
P_L(l) = {
  P   | l=1
  1-P | l=0
  0   | e/w
}

E = P
```

### Example
```
P_M(m) = {
  (1-P) * P | m = 1, 2,...
  0         | e/w
}
E(M) = SUM_m_1_inf((1-p)^(m-1) * P)
SUM_m_1_inf(P_M(m)) = 1
```
What?

eol
