SRC=$(wildcard *.tex)
OUT=$(SRC:.tex=.pdf)
ALL=Cours.pdf

default: ${ALL}

${ALL}: $(OUT)
	python3 -c "__import__('os').system('pdfunite ' + (' '.join(map(lambda i: 'Cours{}.pdf'.format(i), range(1, 11)))) + ' Cours.pdf')"

%.pdf: %.tex
	pdflatex $<
	pdflatex $<

clean:
	rm -f *.aux *.log *.out ${ALL}
