# Slide sources

One Beamer deck per chapter: `codes01.tex` to `codes16.tex`. Styles are in `styles/`; the UTM logo and every figure are in `assets/`.

## Rebuild on Overleaf

1. **Make a zip of the contents of this folder** (not the folder itself), so that `codes01.tex`, `styles/` and `assets/` sit at the top level of the zip. Download the repository from GitHub (Code > Download ZIP), open it, select everything inside `src/` and compress it. The `Makefile` and this README can be left in.
2. In Overleaf choose **New Project > Upload Project** and upload the zip.
3. Open **Menu** (top left) and set:
   - **Compiler**: `pdfLaTeX`
   - **TeX Live version**: 2023 or later
   - **Main document**: the deck you want, for example `codes05.tex`
4. Click **Recompile**. The deck compiles in one run. Recompile once more if the table-of-contents slides are empty: the second pass fills them in.
5. Download the PDF with the download icon above the preview, or **Menu > Download > PDF**.

To build another chapter, change **Main document** in Menu to a different `codesNN.tex` and recompile. All sixteen decks share the same `styles/` and `assets/`, so one project is enough.

### If it does not compile

- *"File `styles/fluxmacros.sty` not found"* or a missing figure: the zip was made from the folder instead of its contents, so everything is one level too deep. Re-zip from inside `src/`, or drag `styles/` and `assets/` to the project root.
- *A missing package*: Overleaf bundles all packages the decks need (`beamer`, `roboto`, `tikz`, `listings`, `booktabs`, `makecell`, `colortbl`). If one is reported missing, raise the TeX Live version in Menu.
- Do not set the compiler to LaTeX, XeLaTeX or LuaLaTeX: the decks are written for pdfLaTeX.

## Rebuild locally

```
make          # all decks; PDFs are copied to ../Slides
make clean    # remove build/
```

or for one deck: `pdflatex codes01` twice.
