R_FILES := $(wildcard *.r)
R_PDFS := $(R_FILES:.r=.pdf)
%.pdf : %.r
	./$<


DOT_FILES := $(wildcard *.dot)
DOT_PDFS := $(DOT_FILES:.dot=.pdf)
%.pdf : %.dot
	dot -T pdf -o $@ $<

SVG_FILES := $(wildcard *.svg)
SVG_PDFS := $(SVG_FILES:.svg=.pdf)
%.pdf : %.svg
	inkscape $< --export-pdf=$@

TEX_FILES := $(wildcard *.tex)
TEX_PDFS := $(SVG_FILES:.tex=.pdf)
%.pdf : %.tex
	pdflatex $<


all : $(R_PDFS) $(DOT_PDFS) $(SVG_PDFS) $(TEX_PDFS)

clean :
	git clean -fx
