# 10/23 lecture notes

## Joint PDFs:
X,Y cont. RVs
P((x,y) in B) = doubleintegral(x, y, f_x,y(x,y) dx dy)
if B is rectangular
P(a <= X <= b /\ c <= Y <=d) = integral(a,b, integral(c,d, f_x,y(x,y) dx dy))
Pr(-inf < X < inf /\ -inf < Y < inf) = integrals -> 1

The joint PDF must add to 1 and is not necessarily bounded by 1.

Each singular PDF also adds to 1 obbviously.

How to obtain the marginal PDF from the joint PDF?

Integrate with respect to the other variable, just like in the discrete case.

f_x(x) = integral(-inf, inf, f_x,y(x,y) dy)

f_x(x) : likelihood / (unit of RV) = likelihood / length
f_x,y(x, y) : likelihood / (unit of RV)^2 = likelihood / area

E[g(x, y)] = doubleintegral(g(x,y) * f_x,y(x,y) dx dy)

X, Y independent if it is product of marginals:
f_x,y(x,y) = f_x(x) * f_y(y)

###Example

POP QUIZ, FUCKING BABAK
