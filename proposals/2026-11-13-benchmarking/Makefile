SRC = $(wildcard *.tex)
PDFS = $(SRC:.tex=.pdf)

all: $(PDFS)

%.pdf: %.tex
	pdflatex -synctex=1 -interaction=nonstopmode -file-line-error $<

clean:
	rm -f *.aux *.log *.out *.synctex.gz

.PHONY: all clean
