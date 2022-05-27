.PHONY: all

all: chordbook.tex chordbook.out cbtitle.sxd 
	pdflatex chordbook.tex
	luatex songidx.lua cbtitle.sxd
	pdflatex chordbook.tex
	pdflatex chordbook.tex
	@echo Compile Successful!
	@cp chordbook.pdf ../release/chordbook.pdf

chordbook.out: chordbook.tex
	pdflatex chordbook.tex

fine: chordbook.tex chordbook.out cbtitle.sxd
	@echo "\documentclass[a4paper,landscape]{book} \usepackage{pdfpages} \input{layout} \begin{document} \includepdf[pages=1-]{chordbook.pdf} \end{document}" > chordbook_tmp.tex
	pdflatex chordbook_tmp.tex
	@echo Compile Successful!
	@cp chordbook_tmp.pdf ../release/chordbook_print.pdf
	@rm chordbook_tmp.*

