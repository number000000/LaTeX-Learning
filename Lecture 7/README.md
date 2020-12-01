Lecture 7 Notes
===============

## Math
## Fraction
```LaTeX
\begin{equation}
\frac{a}{b}
\frac12
\frac{a}2
\end{equation}
```
Output: a/b 1/2 a/b\
You can have any mathematical expression inside {}:
```LaTeX
\begin{equation}
\frac{\frac{a}{b}}{\frac{c+d}{d+e}}
\end{equation}
```
You can use them in inline mode and display mode:
```LaTeX
\(\frac12\) %inline mode
\[\frac12\] %display mode
```

## Tiny fraction
```LaTeX
\[\tfrac12\]
\(\tfrac12\) %looks same as the normal fraction in inline mode: \(\frac12\)
```

## Derivatives
They can be put in display and inline mode.
* Normal derivative:
```LaTeX
\frac{df}{dt}
```
* Partial derivative (curly d):
```LaTeX
\frac{\partial f}{\partial t}
```
* Integrals
```LaTeX
\int_0^2 f(x) dx
```
* Sums
```LaTeX
\sum_{n=0}^7 x_n
```
* Products
```LaTeX
\prod_1^{10} \omega_k
```
## Delimiters
Want to automaticaly resize the expressions that are surrounded by parenthesises? Use `\left``\right` follow the delimiters you want!
```LaTeX
\left(\frac12a+\frac{a+b}{c+d}\right)
```
Compare the above code with `(\frac12a+\frac{a+b}{c+d})` and you will find that the parenthesis is extended so that it can cover the entire expression from top to down.
> Some delimiters:\
> (a), [a], \{a\}, |a|, \|a\|, \langle a \rangle

With the help of this function, we can write a expression of a derivative to the specific value.
```LaTeX
\left. \frac{df}{dx} \right|_{x=0}
```
Note here we use a dot after \left which means that we don't want to put a delimiter here.
