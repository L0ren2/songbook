.PHONY: all

all: chordbook.tex chordbook.out cbtitle.sxd 
	pdflatex chordbook.tex
	luatex songidx.lua cbtitle.sxd
	pdflatex chordbook.tex
	pdflatex chordbook.tex
	echo "Compile Successful!"
	@cp chordbook.pdf ../release/chordbook.pdf
	@pdfjam --nup 2x2 --landscape --paper a4paper --noautoscale true --outfile ../release/chordbook_print.pdf ../release/chordbook.pdf 

chordbook.out: chordbook.tex
	pdflatex chordbook.tex
