CLEAN = *.aux *.log *.lof *.lot *.lol *.out *.toc *.blg *.bbl

thesis.pdf: thesis.tex softlang.cls sources.bib
	pdflatex thesis
	if grep '\citation' *.aux content/*.aux; then bibtex thesis; fi
	pdflatex thesis
	pdflatex thesis

thesis.tex: thesis config.tex content/*.tex Makefile
	./$< > $@

clean:
	rm -f $(CLEAN)
	cd content && rm -f $(CLEAN)

realclean: clean
	rm -f thesis.tex thesis.pdf

.PHONY: clean realclean
