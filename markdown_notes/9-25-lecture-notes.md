# 9/25 Lecture

* Expected Value of a function of a random variable
* Variance of a Random Variable

# EV of function of a random Variable
```
E(X) = Sum(x, x * P_x(x))
E(y)=E[2(x)]^x
y = 2(x)

E(y) = Sum(y, y * P_y(y))
```

If you know probability mass function (P) for X, it's probably hard to find it for Y. So can you use the PMF you already know to get to the value of the E(y) ???

Yes! and this is how:
(note: expected value function uses brackets for some fucking reason)

```
E[g(x)] = Sum(x, g(x) * P_x(x))
```

If you look at the sample space such that only consider those points where g(x) = y, then is this equality true?

```
P_y(y) =Sum({x | g(x)=y}, P_x(x))
```

This is the sum of porbabilities of all sample points such that g(x) = y
Cool. (this derivation is in the textbook)

Looking at:
```
E[g(x)] = E[y]
        = Sum(y, y) * Sum({x | g(x)=y}, P_x(x))
        = Sum(y, Sum({x|g(x)=y}, g(x) * P_x(x)))
        = Sum(x, g(x) * P_x(x))
```

# Variance of an RV

```
var(X) = sigma_x^2 = E[ ( X - E[X] )^2 ]
          ^ why...
```

Oh shit it's the _mean_ of the squared (__difference__ between the __actuals__ and the __mean__), aka literally how much it varies from the mean on average. Pretty straightforward.

SO

The variance of x is...

sigma_x^2 = Sum(x, (x-E[x])^2 * P_x(x))

POP QUIZ
