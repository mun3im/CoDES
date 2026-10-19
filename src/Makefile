# Build all decks into build/, then copy the PDFs to ../Slides
DECKS := $(basename $(wildcard codes??.tex))

all: $(DECKS:%=../Slides/%.pdf)

../Slides/%.pdf: %.tex
	mkdir -p build
	pdflatex -interaction=nonstopmode -output-directory=build $* >/dev/null
	pdflatex -interaction=nonstopmode -output-directory=build $* >/dev/null
	cp build/$*.pdf ../Slides/

clean:
	rm -rf build
