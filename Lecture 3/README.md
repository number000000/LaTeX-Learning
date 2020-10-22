Lecture 3 Notes
===============

## Math Equations
Make math equations in several ways.
* **Command**
```LaTex
My first equation is $F=ma$.
My first equation is \(F=ma\). %This line and the former line will have the same output
My first equation is \[F=ma\]. %This line centered the equation
```
* **Environment**
```LaTeX
My second equation is
\begin{equation}
a=F/m.
\end{equation}
```
In the environment: you can't leave a blank line.
```LaTeX
My second equation is
\begin{equation}
a=F/m.
                           %This is not allowed
\end{equation}
```
## References
* References to the equation:
```LaTeX
My second equation is
\begin{equation}
\label{acce1}
a=F/m.
\end{equation}
and
\begin{equation}
\label{acce2}
F = ma
\end{equation}

I will reference to the equation \ref{acce1} above (\ref{acce2}). %Notice that the output for the second reference will have parentheses
```
* References to the section:
```LaTeX
\section{Method}
\label{my_method}
some text sndjcnidjcn...

In Sec.~\ref{my_method}, we talked about some text.
```
You can also reference subsection in the way how you reference section.\
Notice the `~` before the reference. This will tell the LaTeX don't break the line at here, because if you have a "Sec." at the end of a line and the number at the begining of the next line, that will be weird.
