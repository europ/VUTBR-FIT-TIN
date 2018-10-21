FILE=homework1


.PHONY: make
make: clean
	pdflatex -draftmode $(FILE)
	bibtex $(FILE)
	pdflatex -draftmode $(FILE)
	pdflatex $(FILE)


.PHONY: travis-build
travis-build: clean-all
	pdflatex -halt-on-error -draftmode $(FILE)
	bibtex $(FILE)
	pdflatex -halt-on-error -draftmode $(FILE)
	pdflatex -halt-on-error $(FILE)


.PHONY: clean
clean:
	@rm -fv *.aux *.log *.dvi *.ps *.bbl *.blg *.toc *.out *.lof


.PHONY: clean-all
clean-all: clean
	@rm -fv *.pdf
