

default:
	echo make generated.bib or zip

zip:
	zip guide.zip why3lang.sty generated.bib extra.bib \
		orcid_color-eps-converted-to.pdf

generated.bib: main.aux Makefile
	aux2bib $< > temp.bib
	bib2bib --rename hal url -ob $@ temp.bib
	rm temp.bib

clean:
	rm -f *.aux
