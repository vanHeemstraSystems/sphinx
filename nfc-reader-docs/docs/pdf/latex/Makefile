LATEX_CMD=pdflatex
MAKEINDEX_CMD=makeindex
LATEX_COUNT=8
MANUAL_FILE=refman

all: $(MANUAL_FILE).pdf

pdf: $(MANUAL_FILE).pdf

$(MANUAL_FILE).pdf: clean $(MANUAL_FILE).tex
$(LATEX_CMD) $(MANUAL_FILE)
$(MAKEINDEX_CMD) $(MANUAL_FILE).idx
$(LATEX_CMD) $(MANUAL_FILE)
$(LATEX_CMD) $(MANUAL_FILE)

clean:
rm -f *.ps *.dvi *.aux *.toc *.idx *.ind *.ilg *.log *.out *.brf *.blg *.bbl refman.pdf
