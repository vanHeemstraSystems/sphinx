.PHONY: all pdf clean

LATEX_CMD = pdflatex
MAKEINDEX_CMD = makeindex
LATEX_COUNT = 8
MANUAL_FILE = refman

all: $(MANUAL_FILE).pdf

pdf: $(MANUAL_FILE).pdf

$(MANUAL_FILE).pdf: clean $(MANUAL_FILE).tex
@echo "Generating PDF documentation..."
$(LATEX_CMD) $(MANUAL_FILE)
$(MAKEINDEX_CMD) $(MANUAL_FILE).idx
$(LATEX_CMD) $(MANUAL_FILE)
$(LATEX_CMD) $(MANUAL_FILE)
@echo "PDF generation complete."

clean:
@echo "Cleaning up temporary files..."
rm -f *.ps *.dvi *.aux *.toc *.idx *.ind *.ilg *.log *.out *.brf *.blg *.bbl refman.pdf
@echo "Cleanup complete."
