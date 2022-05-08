.PHONY: all

all: chordbook.tex chordbook.out cbtitle.sxd cbtitle.sbx
	pdflatex chordbook.tex
	luatex songidx.lua cbtitle.sxd
	pdflatex chordbook.tex
	pdflatex chordbook.tex
	echo "Compile Successful!"
	@cp chordbook.pdf ../release/chordbook.pdf
