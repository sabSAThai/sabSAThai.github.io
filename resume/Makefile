all: 1page_resume.pdf

1page_resume.pdf: 1page_resume.tex
	pdflatex -shell-escape 1page_resume.tex

.PHONY: clean
clean:
	$(RM) 1page_resume.pdf \
1page_resume.aux \
1page_resume.bbl \
1page_resume.blg \
1page_resume.log \
1page_resume.out \
1page_resume.pdf \
1page_resume.tex~