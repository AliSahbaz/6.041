# Continuous Random Variables

* Probability __Density__ functions instead of PMFs
* Mean, Variance
* Cumulative Distribution Functions (CDF)

______

## PDF

PDF tells you relative likelihood in different neighborhoods. If you just try to find the pdf at a single point, it is 0. It needs to sum over some region. That is because in a map of the PDF, these are densities. They need to be multiplied by the width of the summing region (integrated).

```
Pr(x < X <= x+d_alpha) = f_x(x) * d_alpha
```

PDFs are values >= 0 (because they are density, obviously).

When you sum PMF, it is 1. The PDF needs to integrate to 1. PDF does not need to be <=1!! Because we're looking at total area under the curve, not the individual values.

### Example:

```
f_x(x) = {
  1/(2 * sqrt(x))   | 0 < x <= 1
  0                 | e/w
}
```

Verify that the integral sum is 1.

(it is)

## Expected Value

```
E(x) = Integral(-inf, inf, x * f_x(x) dx)
                               ^^^^^^^^^ this is the weight
```
That makes this the weighted average, because for every possible value you're multiplying the value by its weight

### Example
What is the expected value of the previous example?

(1/3)

### Example: Uniform PDF

f(x) is a box from -1/2 to 1/2

```
f_x(x) = {
  1 | -1/2 <= x <= 1/2
  0 | e/w
}
```

E(x) of it?

0, by symmetry.

## Variance

Remember, if you know PMF, then Expected value is still obtained by using PMF and you plug in the function

```
Discrete   : E[g(x)] = SUM(x, g(x) * P_x(x))
Continuous : E[g(x)] = Integral(-inf, inf, g(x) * f_x(x) dx)

Variance = E(X^2) - E(X)^2
```

Just like in discrete, that's good.

### Example: variance of same example

Second term drops out because it is 0. First term, calculates to (1/12)

## wat

```
Y = sigma * X + mu
```

sigma dilates the distribution, but a dilation means shorter
mu shifts distribution so that E(x) now = mu

```
Pr(y <= Y <= y+dy) = f_y(y) dy

= Pr(y <= sigma * X + mu <= y + dy)
= Pr((y-mu)/sigma <= X <= (y-mu)/sigma + dy/sigma)
= f_x((y-mu)/sigma) * dy/sigma

d_y(y)=1/sigma * f_x((y-mu)/sigma)
```
