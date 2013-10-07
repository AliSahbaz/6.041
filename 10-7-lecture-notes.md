# 10/7 lecture

* Variance and covariance
* uncorrelated and correlated RVs
* relation to statistical independence
______

### Variance
```
sigma_k^2 = E[(k-E(k))^2]
          = E(k^2 + E(k)^2 - 2*E(k)*k]
          = E(k^2) + E[E(k)] - 2*E[E(k)*k]
          = E(k^2) + E(k)^2 - 2*E(k)^2
var(k) = sigma_k^2 = E(k^2) - E(k)^2
```

This is called the second moment of k.

### Chebyshev's Inequality
The probability that a random variable is away from its mean more than a certain amount c is equal to the variance / c

```
P(|K-E[k]| > c) <= sigma_k^2 / c
```

Takeaway: there's an upper bound on how far you can go from the mean- depends on what you're looking at and the variance.

#### Example: K = alpha (constant)
```
var(K) = 0

P(veer from mean by any amount c) = 0
```

#### Derivation
(k-E(k))^2 IS c^2
Plug this into the equation for variance, take it out of the sums
What you are left with is the summed PMF less than c and greater than c....which is the *total probability* that k is farther than c from the mean

```
<==========|---------|----------|===========>
          E(k)-c    E(k)      E(k)-c
```

So the variance has a direct correlation with the likelihood you're away from the mean.

### Properties of variance

#### How to find var(alpha * K) ?

```
var(alpha * K) = E(k_hat^2) - E(k_hat)^2      (you can take the constant out of Expected value)
               = alpha^2 [E(k^2)-E(k)^2]
```

Takeaway: Variance varies with the square of K

#### How to find var(alpha+ K) ?
The alpha cancels with itself when you subtract squares.

Takeaway: It doesn't affect the variance when you shift your distribution

#### What about two RVs?
```
E(K+L) = E(K) + E(L)
var(K+L) = ???

var(K+L) = E[(K+L-E(K)-E(L))^2]
         = E[(K-E(K))+(L-E(L))^2]
         magic
         = sigma_k^2 + sigma_L^2 + 2*cov(K,L)
```

cov(K,L): covariance: a measure of how the two RVs move relative to each other.

cov(K,L) > 0 is positively correlated
cov(K,L) < 0 is negatively correlated
cov(K,L) = 0 is uncorrelated

```
cov(K,L) := E[(K-E(K))(L-E(L))]
          = E[(KL - K * E(L) - L*E(K) + E(K)*E(L)]
          = E(KL) - E(K)*E(L) - E(L)*E(K) + E(K)*E(L)     when you have E(E(K)) it cancels the inner, so equals E(K)
          = E(KL) - E(K)*E(L)
          = var(K) ?!????????????????
```

When K,L are statistically independent, then K,L uncorrelated
When K,L uncorrelated, hard to prove that also statistically independent.

