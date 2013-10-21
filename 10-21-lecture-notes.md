# PDFs continued

* Dirac Delta
* Gaussians
* PDF Conditioned on Events
* Joint PDFs (time permitting)

## Dirac Delta
Small impulse of stuff. You take the limit as the delta goes to 0, and for some reason this impulse function d(x) always has area **1**.

x=5 w/ Prob 1
f_x(x) = d(x-5)

### Example

x = {
  5 w/ prob 1/2
  -5 w/ prob 1/2
}

How to represent with delta functions?

1/2 [d(x+5) + d(x-5)]

This has a lot to do with signals & systems. Impulses and stuff.

## Gaussian PDF

They gave us a table of Q values and std normal table

Gaussian is a bell shaped curve.

Standard (normalized) Gaussian is the bell curve centered at 0. AKA Normal Density, Standard Normal, etc...

f_x(x) = 1/sqrt(2 * pi) * e^(-x^2/2)

X = X1 + .... Xi
Xi independent and identically distributed

E(X) = 0
var = E(X^2) = integral(-inf, inf, x^2 * f_x(x) dx) = integration by parts boring steps = 1

Pr(X<1)?

You could take integral of -inf to 1.

integral(-inf, 1, f_x(x) dx) = 1/sqrt(2 * pi) * integral(-inf, 1, e^(-x^2/2) dx)

This is hard so we just use the tables we got.

To find this shit we can use the standard normal table, which is -infinity to t, where t is a random point that you're testing.

The Q tables are the CDF, which apparently is t to infinity.

So they're complementary.

### Example
Pr(-1 <= X <= 1)

(Phi(1) - Phi(0)) * 2 = .6826

Pr(-2 <= X <= 2)

(Phi(2) - Phi(0)) * 2 = .9544

### What about Gaussian w/ mean mu and std dev sigma?

Y = sigma * X + mu {
  E(Y) = sigma * E(X) + mu = mu
  sigma_y^2 = sigma^2
}

f_y(y) = 1/sigma * f_x((y-mu)/sigma)

## Conditioning a cont. RV on an event

A: X in Å
Å is a subset of {All Reals}

f_X|A(x) dx = Pr(x <= X <= x + dx | A)

= Pr(x >= X <= x + dx /\ X in Å) / P(X in Å)

= {
  f_x(x) dx / P(A) if X in Å
  0 if X not in Å
}


### Example: Expenonetial RV
What something decays from lambda to 0.

f_x(x) = lambda * e ^ (-lambda * x) * u(x)

u(x) = {
  1   x >= 0
  0   x < 0
}
Unit step function

A = {X | X>t}
f_X|A(x)

P(A) = integral(t, inf, lambda * e^(-lambda * x) dx) = e^(-lambda * t)
f_X|A(x) = {
  f_x(x)/P(A) = lambda * e^(-lambda * x) / e^(-lambda * t)    | x >= t
  0                                                           | e/w
}
