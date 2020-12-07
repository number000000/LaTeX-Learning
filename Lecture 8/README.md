Lecture 8 Notes
===============

## Set the size of delimiters you want
```LaTeX
\[
( \big( \Big( \bigg( \Bigg(
\]
```
Size: from small to big

## Matrices
Need to put into display math mode:\
Matrix with no parenthesis:
```LaTeX
...
\usepackage{amsmath}
...

\[
\begin{matrix}
  a & b & c \\  %& is a alignment character
  d & e & f \\
  g & h & i
\end{matrix}
\]
```
Matrix with parenthesis:
```LaTeX
\[
\begin{pmatrix}
  a & b & c \\
  d & e & f \\
  g & h & i
\end{pmatrix}
\]
```
Matrix with something before it:
```LaTeX
\[
2A+3\times\begin{pmatrix}
  a & b & c \\
  d & e & f \\
  g & h & i
\end{pmatrix}
=0
\]
```
Matrix with determinant:
```LaTeX
\[
\begin{vmatrix}
  a & b & c \\
  d & e & f \\
  g & h & i
\end{vmatrix}
\]
```
Matrix with other delimiters:
```LaTeX
\[
left(\begin{matrix}
  a & b & c \\
  d & e & f \\
  g & h & i
\end{matrix}\right]
\]
```
Matrix with arbitrary size:
```LaTeX
\[
\begin{pmatrix}
  a_{11} & \cdots & a_{1n} \\  %& is a alignment character
  a_{21} & \cdots & a_{2n} \\
  \vdots & \ddots & \vdots \\
  a_{31} & \cdots & a_{3n}
\end{pmatrix}
\]
```

## Array
It is quite similar to matrix environment.\
But it will have one more argument that determines the spaces of each element.
```LaTeX
\[
\begin{array}{ccc} %ccc tells LaTeX to center justify the columns
-a & -b & c \\
d & e & f \\
g & h & i
\end{array}
\]

\[
\begin{array}{rrr} %ccc tells LaTeX to right justify the columns
-a & -b & c \\
d & e & f \\
g & h & i
\end{array}
\]

\[
\begin{array}{lll} %ccc tells LaTeX to left justify the columns
-a & -b & c \\
d & e & f \\
g & h & i
\end{array}
\]

\[
\begin{array}{lrc} %lrc tells LaTeX to left justify the first column, right justify the second column, and center justify the third column
-a & -b & c \\
d & e & f \\
g & h & i
\end{array}
\]

\[
\begin{array}{r|rr} % r|rr will output a "|" to seperate the first and second column
-a & -b & c \\
d-- & e-- & f-- \\
g & h & i
\end{array}
\]

\[
\begin{array}{r|rr} 
-a & -b & c \\
\hline  %draw horizontal line
d-- & e-- & f-- \\
\hline
g & h & i
\end{array}
\]

\[
\begin{array}{r|rr} 
-a & -b & -c \\
\hline \\ [-1em]  %[-1em] add a new empty line with negative space to adjust space
d & e & f \\
\hline
g & h & i
\end{array}
\]
```
