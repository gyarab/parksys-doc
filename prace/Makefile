export TEXINPUTS=../tex//:

all: prace.pdf

# LaTeX je potreba spustit nekolikrat, aby spravne spocital odkazy
prace.pdf: prace.tex $(wildcard *.tex) literatura.bib prace.xmpdata
	pdflatex $<
	bibtex prace
	pdflatex $<
	pdflatex $<

clean:
	rm -f *.log *.dvi *.aux *.toc *.lof *.lot *.out *.bbl *.blg *.xmpi
	rm -f kapitoly/*.log kapitoly/*.dvi kapitoly/*.aux kapitoly/*.toc kapitoly/*.lof kapitoly/*.lot kapitoly/*.out kapitoly/*.bbl kapitoly/*.blg kapitoly/*.xmpi
	rm -f prace.pdf
