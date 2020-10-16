Lecture 2 Notes
===============

## LeTeX commands: 
start with \ followed by the name of the command (letters only) and arguments inside {}

## Switches:
Switches is limited to the group inside {}\
Ex. \bf is the boldface command

## Comments:
Anything follows % will be comments\
Ex: 
```LaTeX
%This is a comment
```

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

## Debug
#### Option 1: Help
Type "?" and hit return, you can get a list of option you can choose:\
![Help](/Images/Lecture 1 - Help.jpg)
#### Option 2: Go on
Hit return\
Notice that there is a outout pdf file saved to where your project is saved.\
![Go on](/Images/Lecture 1 - Go on.jpg)
#### Option 3: Quit
Type "x" and hit the return, the compiler stops and the console shows this message:\
![Quit](/Images/Lecture 1 - Quit.jpg)

## Some syntaxs for LaTeX:
* **Characters:** A-Z, a-z, 0-9, some symbols except reserved characters
* **Reserved characters:** # $ % ^ & _ {} ~ \
* **Grouping things using curly brackets {}**\
{\bf This is bold.} This is no longer bold. -----> **This is bold.** This is no longer bold.
* **Commands:**\
\ + name of the command + {argument}\
***ex.** \hspace{1in} -----> leave horizontal space for 1 inch (1in can be 1cm, which means 1 centimeter)*\
      *Hello \hspace{1in} world! -----> Hello             world!*
