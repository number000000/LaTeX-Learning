Lecture 5 Notes
===============

## bibliography
```LaTeX
\begin{thebibliography}{99}
```
The ``99`` here is the maximum citation you want to enter into the your article.\
Telling LaTex about the maximum citation you want to enter, LaTex will automatically leave spaces. For example, if your maximum citation is 99:
```LaTeX
Reference:
 [1] aaaaaaa %you will get spaces before the one digit number
[99] bbbbbbb
```

### BibTeX
It allows us to store bibliography files and reuse it in many documents. They are databases. Only references you need are used.
1. Make one new plain text bibliography files, extension ``.bib``. Remember to save it in the same folder where your documents that want to use it is.
2. Include ``\cite{bibitemlabel}`` in text
3. Include ``\bibliographystyle{plain}`` and ``\bibliography{samplebib1, samplebib2}`` before ``\end{document}``. (samplebib1 and samplebib2 are the names of your bib files).
4. Typset pdfLaTeX. Then run BibTeX. Then typeset twice with pdfLaTeX.
* **Note** ``\bibliographystyle{plain}``: ``plain`` is a BibTeX style. It can also be ``alpha``, ``abbrv`` and so on.

Things you put into the BibTeX:
```LaTeX
@article{climateChange,
  title={Assessing the impact of climate change on extreme fire weather events over southeastern Australia},
  author={Hasson, AEA and Mills, GA and Timbal, B and Walsh, K},
  journal={Climate Research},
  volume={39},
  number={2},
  pages={159--172},
  year={2009}
}
```
``{}`` can be ``""``.\
``cilmateChange`` is the label of the citation. You can refer to this citation using this label in your article. \
