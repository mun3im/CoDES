# CoDES: Contemporary Digital Electronic Systems

Lecture slides for *Contemporary Digital Electronic Systems* (Fourth Edition, 2026; slides track Release E4b, the corrected reprint) by Mun'im Zabidi and Ab al-Hadi Ab Rahman, the learning module for **SKEE1233** at Universiti Teknologi Malaysia.

## About the book

The book is a first course in digital logic for undergraduates in electrical, electronic, computer and mechatronics engineering. It assumes only secondary-school algebra and basic ideas of voltage and current. Sixteen chapters build up in layers, each using the results of the one before:

| Layer | Chapters | Content |
|---|---|---|
| Representation | 1-3 | Analog vs. digital; binary, octal, hex; signed and real numbers |
| Combinational logic | 4-7 | Gates, Boolean algebra, Karnaugh maps, design procedure |
| Combinational modules | 8-9 | Multiplexers, decoders, adders, comparators |
| Storage | 10-11 | Latches, flip-flops, registers |
| Sequential modules | 12 | Counters |
| State machines | 13-15 | FSM design, analysis, controllers |
| Hardware description | 16 | Synthesizable Verilog |

Every chapter opens with a motivation, measurable learning outcomes and a guiding question, and closes with a summary and exercises. The Fourth Edition separates the logic abstraction from electrical reality: gates and flip-flops are first idealized, then delay, noise margins and setup and hold times show where the abstraction breaks down.

## About the slides

The `Slides/` folder holds one compiled Beamer deck (PDF) per chapter, `codes01` to `codes16`, in the Flux theme (hunter-green variant). Their structure, a deck-by-deck page list and the styling are described in [`Slides/README.md`](Slides/README.md).

## Repository layout

```
Slides/                         compiled slides, codes01.pdf ... codes16.pdf
src/
  codes01.tex ... codes16.tex   slide sources
  styles/                       Flux theme files (hunter-green style added)
  assets/                       UTM logo and all figures
  Makefile                      builds every deck and copies the PDFs to ../Slides
```

## Building the slides

From `src/`, run `make` to build all sixteen decks (each is compiled twice, the second pass fills in the table of contents). The PDFs are copied to `Slides/`. To build one deck by hand:

```
cd src
pdflatex codes01
pdflatex codes01
```

You need a TeX distribution with the `beamer`, `roboto`, `tikz`, `listings` (with its Verilog language definition), `booktabs`, `makecell` and `colortbl` packages. Figures are read from `src/assets/` through `\graphicspath`.

## License

MIT License. See `LICENSE`.
