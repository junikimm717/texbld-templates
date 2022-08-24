%.pdf:
	latexmk -pdf $*.tex

PDFTARGETS=main.pdf

TARGETS=$(PDFTARGETS)

pdf: $(PDFTARGETS)

all: $(TARGETS)

clean:
	rm -rf $(TARGETS)

wipe:
	rm -rf ./pythontex-files-main
	ls main.* | grep -vE "^main\.(bib|tex)$$" | xargs -r rm -rf

watch:
	latexmk -pdf -pvc
	
.PHONY: pdf docx all clean junk watch wipe
