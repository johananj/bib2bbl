Sometime journals expect bbl rather than bib. This is a template to generate bbl from bib. 

# How To
- Find lines with `\cite` in your original tex file, and paste them on a separate file. 
	+ `grep -h "\cite{" source.tex > destination.tex`
- Move these lines to the `document.tex` template in this repository. 
- Include the corresponding `.sty` and `.bst` files.
- Paste a copy of your bib file in this folder, or paste them inside `references.bib`.
- Compile with `compile.sh`
- The `document.bbl` file will be produced, which will contain the bbl entries.
- Paste these bbl entires between `\begin{thebibliography}{}` and `\end{thebibliography}` in your original tex file.
- It is better to do this process at the end, and there would not be any issues with the order of the citation.

