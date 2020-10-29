Lecture 4 Notes
===============

## List
```LaTeX
\begin{itemize}
\item First line.
\item[-] Second line.
\item[*] Third line.
\item[$>$] etc
\end{itemize}
```
Get a result:
```LaTeX
· First line.
- Second line.
* Third line.
> etc
```
If you want to change the item symbol for the whole document:
```LaTeX
\renewcommand{\labelitemi}{command}
```
Make sure that this line goes before the first ``\begin{itemize} ``. It can go into the **preamble**.\
Command can be ``\textgreater`` for ">", ``$\bullet$`` for "·", ``$\star$`` for "*".

> **Preamble:**
 Things that you put between the ``\documentclass`` and the ``\begin{document}``

##### A example for List:
```LaTeX
\documentclass{article}

\renewcommand{\labelitemi}{$\bullet$} %preamble

\begin{document}

\begin{itemize}
\item the first entry here
\item try
\item[-] Second line.
\item[*] Third line.
\item[$>$] etc
\end{itemize}

\renewcommand{\labelitemi}{\textgreater}

\begin{itemize}
\item the first entry here
\item Second line.
\item Third line.
\item etc
\end{itemize}

\end{document}
```
Output:
```LaTeX
· the first entry here
· try
- Second line.
* Third line.
> etc
> the first entry here
> Second line.
> Third line.
> etc
```

## Nested List
```LaTeX
\begin{itemize}
\item a
\begin{itemize}
\item a
\end{itemize}
\item a
\end{itemize}
```
Output:
```LaTeX
· a
  - a
  - a
· a
```
### Defaulting nested list
```LaTeX
\renewcommand{\labelitemi}{\textgreater}
\renewcommand{\labelitemii}{$\star$}
\renewcommand{\labelitemiii}{$\bullet$}
```
A list would be looking like:
```LaTeX
> hey
  * nested
    · list
```
The number of i in the ``{\labelitemi}`` denotes the level of the list in a nested list.

## Numbered List
```LaTeX
\begin{enumerate}
\item hey
\begin{enumerate}
\item inner one
\end{enumerate}
\item two
\end{enumerate}
```
Output:
```LaTeX
1. hey
  (a) inner one
2. two
```

### Defaulting nested numbered list
We use a package ``enumerate``. It allows us to have "[]"after the begin command.
```LaTeX
\usepackage{enumerate}
...
\begin{document}
...
\begin{enumerate}[(i)]
\item hey
\begin{enumerate}[1]
\item inner one
\item inner two
\end{enumerate}
\item cooool
\end{enumerate}
```
Output:
```LaTeX
(i) hey
  1 inner one
  2 inner two
(ii) cooool
```
We can put these things in []:
1. ``A`` Give us uppercase ABCD...
2. ``a`` Give us lowercase abcd...
3. ``I`` Give us uppercase I II III ...
4. ``i`` Give us lowercase i ii iii...
5. ``1`` Give us numbers 1234...

If you want to use a special character as a literal text, you should enclose it in curly brackets:
```LaTeX
\begin{enumerate}[Excerc{i}se 1]
\item hey
\begin{enumerate}[Excercise 1]
\item inner one
\item inner two
\end{enumerate}
\item two
\end{enumerate}
```
Output:
```LaTeX
Excercise 1 hey
  Excerc1se 1 inner one
  Excerc2se 2 inner two
Excercise 2 two
```
There are other kinds of packages like ``enumitem`` that has more complicated functions.

## Description List
```LaTeX
\begin{description}
\item[First] we add this.
\item[Second] we minus this.
\item[Last] we are done.
\end{description}
```
Output:\
**First** we add this.\
**Second** we minus this.\
**Last** we are done.\

The argument ``[First]`` is optional.

## Color
```LaTeX
\usepackage{color}

\begin{document}

\begin{description}
\item[\color{red} First] we add this.
\item[\color{blue} Second] we minus this.
\item[Last] we are done.
\end{description}
```
Output:
![Colored list](https://github.com/number000000/LaTeX-Learning/blob/main/Images/Lecture%204%20-%20Colored%20List.JPG)

## Bibliography
```LaTeX
\begin{document}

Some random text\cite{article1}. Some random text\cite{article2}.

\begin{thebibliography}{99}
\bibitem{article1}
a citation of an article

\bibitem{article2}
a citation of another article
\end{thebibliography}

\end{document}
```
Output:
![bibliography]()
