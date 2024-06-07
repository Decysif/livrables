

default:
	echo make generated.bib

generated.bib: main.aux Makefile
	aux2bib $< > temp.bib
	bib2bib --rename hal url -ob $@ temp.bib
	rm temp.bib

clean:
	rm -f *.aux
