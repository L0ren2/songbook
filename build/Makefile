.PHONY: all

all: chordbook.tex chordbook.out cbtitle.sxd 
	pdflatex chordbook.tex
	luatex songidx.lua cbtitle.sxd
	pdflatex chordbook.tex
	pdflatex chordbook.tex
	echo "Compile Successful!"
	@cp chordbook.pdf ../release/chordbook.pdf

chordbook.out: chordbook.tex
	pdflatex chordbook.tex
