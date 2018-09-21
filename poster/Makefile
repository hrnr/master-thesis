all: poster.pdf

poster.pdf: poster.tex $(wildcard *.tex)
	pdflatex $<

clean:
	rm -f *.log *.dvi *.aux *.toc *.lof *.lot *.out *.bbl *.blg *.acn *.glo *.glsdefs *.ist *.acr *.alg *.glg *.gls
