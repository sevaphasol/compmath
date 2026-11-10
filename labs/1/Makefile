LATEXMK ?= latexmk
REPORT := report
FIGURES := $(wildcard figures/*.png)

.PHONY: all clean
.DELETE_ON_ERROR:

all: $(REPORT).pdf

$(REPORT).pdf: $(REPORT).tex $(FIGURES)
	$(LATEXMK) -pdf -interaction=nonstopmode -halt-on-error -file-line-error $<
	$(LATEXMK) -c $(REPORT).tex

clean:
	$(LATEXMK) -c $(REPORT).tex
