Note: I missed the previous lecture, but it covered conditional probability applied to expected value / variance

# Lecture 10/2

Day before the test oh fuck

* Joint PMFs
* Mean of functions of multiple Random Variables
* Variance for functions of multiple RVs

______

## Joint PMF

For problems with two independent variables, like taking the sample of the class's weights and heights,

```
P_x,y (x, y) = Pr(X=x /\ Y=y)
```

Example:

Plot some shit

```
  Y
  |      x
  |   x  x
--|x--x--x-------------X
  |   x  x
  |      x
  1/3
     1/9
        1/15
```

```
0 <= P_x,y(x, y) <= 1

SUM(x, SUM(y, P_x,y(x, y) ) ) should equal 1
```

So...what is:

```
P_x(1) = ?
```

If you sum over all the Y's, then you'll have the total value of X

So

```
P_x(1) = P_x,y(1, -1) + P_x,y(1, 0) + P_x,y(1, 1) = SUM(y, P_x,y(1, y))

```

So..

```
P_x(x) = SUM(y, P_x,y(x, y)) is the Marginal PMF for X
P_y(y) = SUM(x, P_x,y(x,y)) is the Marginal PMF for Y
```

So what is this?
```
P_X|Y(x|y) = P(X=x | Y=y)
```

You can break this down with BAYEeEEeS + intersection equivalence shit

```
P(A|B) = P(A /\ B) / P(B)
```

So

```
P_X|Y(x|y) = P(X=x | Y=y)             <<<< remember P(A and B) = P(A) * P(A | B)
           = P(X=x /\ Y=y) / P(Y=y)   <<<< and because P_x,y (x, y) = Pr(X=x /\ Y=y),
           = P(P_x,y(x, y)) / P_y(y)

hinges on the fact that P_y(y) > 0
```

So we can find

### P_x(x) = ?
```
       = SUM(y, P_x,y(x,y))
```

What you're doing here is "flattening" against an axis. This case you're flattening to the X axis, so at each possible point you sum the probabilities. It ends up being (1/3, 1/3, 1/3)

### P_y(y) = ?
```
       = SUM(x, P_x,y(x,y))
       = 1
```

Flattening against Y axis, so you get (3/45, 8/45, 23/45, 8/45, 3/45).

### P_x|y(x|y=0) = ?

```
Remember that P_X|Y(x|y) = P_x,y(x,y) / P_y(y)

So you divide the intersection by P_y(0)

AKA normalize the points in your conditioned universe (ie y=0) so that the P_x|y sum = 1
```

## Independence
```
P_x|y(x|y) = P_x(x)
```

As before, when the conditional probability is equal to the individual probability, then the events are independent

So

```
P_x,y(x,y) / P_y(y)
= P_x(x) => P_x,y
```

To test for independence do a quick example
```
P_x,y(0, 2) = P_x(0) * P_y(2) ?
```
If so then independent
If not then dependent

## Expected Value of functions of multiple random variables
E(X+Y) = SUM(x, SUM(y, (x+y) * P_x,y(x,y)))
       = SUM(x, SUM(y, [x * P_x,y(x,y) + y * P_x,y(x,y)] ))
       = SUM(x, SUM(y, P_x,y(x,y)) + SUM(y, y * SUM(x, P_x,y(x,y))))
                  ^ P_x(x)                          ^ P_y(y)

E(X+Y) = E(X) + E(Y)

### example
Mean of the binomial PMF
  L: # of successes in n independent trials
  E(L) = SUM(l, l * combination(n, l) * P^l * (1-p)^(n-l))  < wtf?

K_i {
  1 if success
  0 if failure
}

P -> 1
1-P -> 0

E(Ki) = P
L = K1 + K2 + ... + Kn => E(L) = np


What the fuck just happened
