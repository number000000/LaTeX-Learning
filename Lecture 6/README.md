Lecture 6 Notes
===============

## Package: amsmath (American Standard Math)
```LaTeX
\usepackage{amsmath}
```
Insert this line in the preamble, which is after the `\documentclass`.\
Then use this format to write your equation:
```LaTeX
\begin{equation}
F = ma
\end{equation}
```
If you don't want to use package, you can use `\nonumber`after the equation in the equation environment.\
### Long equation
If an equation is too long to fit in one line. Write:
```LaTeX
\begin{multline}
a=aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa\\
aaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
\end{multline}
```
The following lines makes an equation without the equation number after the equation.
```LaTeX
\begin{multline*}
a=aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa\\
aaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
\end{multline*}
```
### Many equations
```LaTeX
\begin{equation}
\label{equations}
\begin{split}
a+b&=c\\  % the "&" aligns the "=" in the output
e+f&=g
\end{split}
\end{equation}
```
Notice this implementation only gives one equation number to all of the equations that use it. So a+b=c and e+f=g get a same equation number. To reference these two equation, we can write the following in your article.
```LaTeX
I get two equations, they are (\ref{equations}).
```
If you want to have a equation number for each equation you put. Use:
```LaTeX
\begin{align}
\label{equation1}
a+b&=c\\
\label{equation2}
e+f&=g
\end{align}
```
To reference it, write:
```LaTeX
I got two equations, they are (\ref{equation1}) and (\ref{equation2}).
```
If you want two or more equation each line, you can do this:
```LaTeX
\begin{align}
\label{equation1}
a+b&=c & c&=a+b\\
\label{equation2}
h+p&=c & l+w+q&=a+b
\end{align}
```
The way to reference them is the same as above.

> Don't want to write () around \ref{...} to make a reference with ()? Try this:
> `\eqref{yourLable}`

## Some Syntax for Math Equation
### power / superscript
```LaTeX
\begin{equation}
E=mc^{12}
\end{equation}
%Or
\[E=mc^{12}\]

\[E=mc^12\] %gets E=m(c^1)2 instead of E=mc^(12)
```
### Subscript
```LaTeX
\begin{equation}
E_1^2=mc_{12} %Notice "E": you can combine subscript and superscript together!
\end{equation}
```
### Greek Letters
Lowercase greek letters:
```LaTeX
\begin{equation}
\alpha + \beta = \gamma + \delta
\end{equation}
```
Uppercase greek letters:
```LaTeX
\begin{equation}
A + B = \Gamma + \Delta
\end{equation}
```
**Notice**: Uppercase alpha and beta are the same as A and B in English.
For letters that have multiple versions:
```LaTeX
...
\epsilon + \varepsilon = \theta + \vartheta = \phi + \varphi
...
```
### Math Symbols
```LaTeX
a \ge b \le c  % a >= b <= c
a \equiv b
b \ll c
...
```
There are too many of them. Consult the complete list of math symbols in the Wikibook.

## Package: amssymb
This package gives you additional math symbols that the basic set doesn't have.
For example:
```LaTeX
\begin{equation}
a \gtrsim b \lesssim c \hbar
\end{equation}
```

## Package: wasysym
Some weird symbols:
```LaTeX
Symbol for mercury: \mercury, and symbol for earth: \earth.
```
\
There are many symbols you can use. Just check **Comprehensive LaTeX Symbol List** or **Detexify (A website)**.
