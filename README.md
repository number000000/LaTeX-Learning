# LaTeX-Learning

## Tables: The Tabular Environment
Last time, we learned array for math mode. Now, we will learn table for text mode.\
We will use `tabular` environment instead of `array` from last time.
```LaTeX
\begin{document}
Here is a table:
\begin{tabular}{r||r|r}
header -a & header -b & header c \\
\hline \hline
entry d-a & entry e-b & entry f-c \\
\hline
entry h & entry g & entry i
\end{tabular}
\end{document}
```
Justification character: `p{dimension}` p is paragraph and dimension is how wide the paragraph(column) is.
```LaTeX
\begin{tabular}{r||r|p{1in}}
header -a & header -b & header c \\
\hline \hline
entry d-a & entry e-b & Arantes do Nascimento (Pele) \\
\hline
entry h & entry g & entry i
\end{tabular}
```
But because it is left-right justified, the "Arantes do Nascimento (Pele)" may spaced a little weird. So you want to add `\newline` between `Arantes` and `do` to manualy creat a new line.

## Floats and Graphics
What is a float?\
A float is a frame where you can put into tables, pictures ... Why it's called float because it can finds a place to land in your document where LaTeX decides. But you can also nudge it into place where you want.
### Table environment
`table` is a float. It automatically places the table and table number for referencing, including a caption.\
Note: `tabular` make the table, not `table`
```LaTeX
This is table~\ref{mytable}
\begin{table}[b]
\begin{center}
\begin{tabular}{|c||l|p{1in}|}
...
\end{tabular}
\end{center}
\caption{ \label{mytable}
This table shows blah blah}
\end{table}
```
`[b]` means placing the table to the bottom of the page. You can replace it with `[h]` for here, `[t]` for at the top of the page.

```LaTeX
\listoftables %gives you a list of tables you have in the document
```
### Graphics
```LaTeX
% in the preamble
\usepackage{graphicx}
```
With this package, we can use the command `\includegraphics[attributes]{filename}` to insert pictures.\
You want to insert a picture, you save the picture in the same folder where your .tex file is. Then use the command `\includegraphics{filename}`. If it is too large, put `width=xin` into the attributes part, x is the number of inches you want.\
Other attributes: `[height=...]``[scale=...]``[trim=l b r t]`. When have multiple attributes, place them like this `[attributes1=..., attributes2=..., ...]`

#### Figure Environment
It is analogous to the table environment. But it is for pictures.
```LaTeX
In this figure~\ref{picture}:
\begin{figure}[t]
\begin{center}
\includegraphics[attributes]{filename}
\end{center}
\caption{\label{picture} This is a picture about blah blah blah}
\end{figure}
```
```LaTeX
\listoffigures %gives you a list of firgures you have in the document
```
