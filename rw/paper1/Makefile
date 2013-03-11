PDFLATEXARGS = -file-line-error -halt-on-error

.PHONY: clean all

all: rw.pdf

rw.pdf: rw.tex rw.bbl
	pdflatex $(PDFLATEXARGS) rw.tex; pdflatex $(PDFLATEXARGS) rw.tex
        
rw.bbl: rw.tex bib.bib
	pdflatex $(PDFLATEXARGS) rw.tex; bibtex rw; rm rw.pdf

clean:
	rm *.pdf *.bbl *.out *.aux *~ *.blg

