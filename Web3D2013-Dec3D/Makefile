Default: pre clean
	open paper.pdf

pre:
	pdflatex paper 
	bibtex paper
	pdflatex paper
	pdflatex paper

print:
	latex paper
	bibtex paper
	latex paper
	latex paper
	latex paper
	dvips -Ppdf -t letter -G0 -o paper.ps paper.dvi
	#ps2pdf -dPDFSETTINGS#/prepress -dCompatibilityLevel#1.3 -dAutoFilterColorImages#false -dAutoFilterGrayImages#false -dColorImageFilter#/FlateEncode -dGrayImageFilter#/FlateEncode -dMonoImageFilter#/FlateEncode -dDownsampleColorImages#false -dDownsampleGrayImages#false paper.ps paper.pdf
	ps2pdf -dPDFSETTINGS#/prepress -dCompatibilityLevel#1.3 paper.ps paper.pdf

clean:
	rm -rf *.lot *.lbl *.tec *.aux *.log *.bbl *.blg *.ps *.toc *.out *.lof *.dvi *~
