# Conditional PDFs

## X,Y continuous Random Variables

```
f_x,y(x,y) is the PDF
A_x: x0 <= X <= x0 + d_x
Ay: y0 <= y <= y0+d_y
```

So we plot this shit on a graph and they both have restrictions on their axes so you get a rectangle or some shit.

So now we want to do conditionals on one of the axes to find the other fuck are you serious
```
P(Ax | Ay) = P(A_x /\ A_y)/P(A_y) = f_x,y(x0y0) * d_x * d_y / f_y(y0) * d_y
^
f_X|Y(x0|y0) * d_x

f_X|Y(x|y) = f_x,y(x,y)/f_y(y)    | f_y(y)>0

integral from -inf to inf of (f_X|Y(x|y)) dx = integral f_x,y(x,y)/f_y(y) dx
                                             = 1/f_y(y) * integral f_x,y(x,y) dx
                                                                ^ f_y(y) = 1
```

## Ex: triangle

```
x=1-y

f_X,Y(x,y) = c = 2
           = 0 elsewhere
```

f_X|Y(x|y)?
E(X|Y)?
var(X|Y)?

Apparently you drop a fucking guillotine on the plot straight across and you call that shit y=y0 and x=1-y0

Then you take your values from that or something fuck.

## Baye's rule:

```
f_X|Y(x|y) = f_Y|X(y|x) * f_x(x) / f_Y(y)
```

x continuous
y discrete

```
f_X|Y(x|y) = f_X(x) * P_Y|X(y|x) / P_Y(y)
```

## Iterated expectations

```
E(X) = E_y[E_x(X|Y)]
```

## Law of total variance

```
var(X) = E[var(X|Y)] + var[E(X|Y)]
```

## Example: Stick breaking

|===========================X===========|
0                                       l

X: |===============X========|
   0                        x

Y: |========================|
   0                        y

Uhh I don't know. Exam on Thursday.
