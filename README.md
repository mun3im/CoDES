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

The `Slides/` folder holds one Beamer deck per chapter for all sixteen chapters (`codes01` to `codes16`).

Each deck follows the same pattern:

1. **Why this chapter** and the learning outcomes.
2. **An opening question** that the deck answers near the end.
3. **Content sections** that follow the chapter, reusing the book's worked examples and figures.
4. **Summary** and a pointer to the next chapter.

A table-of-contents slide marks the start of each section. Exercises are not included. The Chapter 16 deck shows the Verilog examples as syntax-colored listings.

| Deck | Chapter | Pages |
|---|---|---|
| `codes01` | Introduction | 24 |
| `codes02` | Number Systems I | 31 |
| `codes03` | Number Systems II | 30 |
| `codes04` | Logic Gates | 40 |
| `codes05` | Boolean Algebra | 34 |
| `codes06` | Karnaugh Maps | 32 |
| `codes07` | Combinational Logic Design | 29 |
| `codes08` | Standard Combinational Modules | 34 |
| `codes09` | Arithmetic Circuits | 37 |
| `codes10` | Latches and Flip-Flops | 38 |
| `codes11` | Registers and Shift Registers | 31 |
| `codes12` | Counters | 24 |
| `codes13` | Finite State Machines | 32 |
| `codes14` | FSM Analysis | 21 |
| `codes15` | FSM Controllers | 35 |
| `codes16` | First Steps in Verilog | 32 |

The slides use the Flux Beamer theme (hunter-green variant) at 16:9, Roboto font, with the UTM logo.

## Repository layout

```
Slides/
  codes01.tex ... codes16.tex   slide sources
  codes01.pdf ... codes16.pdf   compiled slides
  styles/                       Flux theme files (hunter-green style added)
  assets/                       UTM logo
fig/                            figures used by the slides
```

## Building the slides

Run `pdflatex` twice from inside `Slides/` (the second pass fills in the table of contents):

```
cd Slides
pdflatex codes01
pdflatex codes01
```

You need a TeX distribution with the `beamer`, `roboto`, `tikz`, `listings` (with its Verilog language definition), `booktabs`, `makecell` and `colortbl` packages. Figures are read from `../fig/` through `\graphicspath`.

## License

MIT License. See `LICENSE`.
