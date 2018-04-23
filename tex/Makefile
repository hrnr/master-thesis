export TEXINPUTS=../tex//:

all: thesis.pdf

# LaTeX must be run multiple times to get references right
thesis.pdf: thesis.tex $(wildcard *.tex) bibliography.bib thesis.xmpdata
	pdflatex -draftmode -synctex=1 $<
	bibtex thesis
	makeglossaries thesis
	pdflatex -draftmode -synctex=1 $<
	pdflatex -synctex=1 $<

clean:
	rm -f *.log *.dvi *.aux *.toc *.lof *.lot *.out *.bbl *.blg *.xmpi *.acn *.glo *.glsdefs *.ist *.acr *.alg *.glg *.gls
	rm -f thesis.pdf
