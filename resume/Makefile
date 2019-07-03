all: cv.pdf

cv.pdf: cv.tex
	pdflatex -shell-escape cv.tex

.PHONY: clean
clean:
	$(RM) cv.pdf \
main.aux \
main.bbl \
main.blg \
main.log \
main.out \
main.pdf \
main.tex~