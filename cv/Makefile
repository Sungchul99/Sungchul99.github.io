HOMEPAGE ?= ..

cv.pdf: cv.tex
	latexmk -pdf -interaction=nonstopmode -halt-on-error cv.tex

# Copy the PDF into the homepage, where /cv/ embeds it.
publish: cv.pdf
	mkdir -p $(HOMEPAGE)/files
	cp cv.pdf $(HOMEPAGE)/files/cv.pdf

clean:
	latexmk -c cv.tex

.PHONY: publish clean
