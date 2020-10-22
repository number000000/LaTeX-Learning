Lecture 2 Notes
===============

## LaTeX commands: 
start with \ followed by the name of the command (letters only) and arguments inside {}

## Switches:
Switches is limited to the group inside {}\
Ex. \bf is the boldface command

## Comments:
Anything follows % will be comment\
Ex: 
```LaTeX
%This is a comment
```
## Tool we use: Texworks
Texworks calls LaTeX (Texworks is like IDE). Texworks also contains a PDF viewer. Texworks has a rudimentary text editor.

## LaTeX Environment:
```LaTeX
\begin{EnvironmentName}
text to be influenced
\end{EnvironmentName}
```
Example:
```LaTeX
\documentsclass{article}
\begin{document}
\begin{center}
Hello world % Hellow world will be centered
\end{center}
\end{document}
```

## LaTeX files:
* `first_project.tex`: LaTeX file
* `first_project.pdf`: PDF file
* `first_project.log`: Plain text: log-file (warnings, errors)
* `first_project.aux`: aux stands for **auxilliary**. Plain text: keeps track of internals

## LaTeX packages:
Packages enhance the capabilities of LaTeX. 
Package can take option too.
```LaTeX
\usepackage[options]{packagename1}
\usepackage[options]{packagename2}
\usepackage{packagename3, packagename4, packagename5}
```
color package:
```LaTeX
\documentclass{...}

\usepackage{color} % use package

\begin{document}
\end{document}
```
```LaTeX
Hello {color{red} World} again! %"World" will be red.
```

## Code syntax:
documentclass takes two arguments:
```LaTeX
\documentclass[optional]{class}
```
Class: book, article, extarticle, letter\
Option: you can have many options seperated by commas
Ex.
```LaTeX
\documentclass[letterpaper, notitlepage, 10pt]{article}
```

## Line breaks
* blank line between two paragraphs should make two paragraphs:
```LaTeX
...
paragraph one with some texts

paragraph two with some texts
...
```
* `\\`:
```LaTex
The line should break after\\ this.
```
* `\break`:
```LaTeX
This line should break after \break this and have a weird spacing format.
```
* `\hfil\break`:
```LaTeX
This line won't have \hfil\break weird spacing format.
```

## Section
Format your section title
```LaTex
\section{Name of the section}
\subsection{Name of the smaller section}
```
## Begin in a new page
```LaTeX
\newpage
```
