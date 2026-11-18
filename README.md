# NDS Thesis Layout
[![Document Build](https://github.com/RUB-NDS/thesis_layout/actions/workflows/compile-thesis.yml/badge.svg)](https://github.com/RUB-NDS/thesis_layout/actions/workflows/compile-thesis.yml)

Latex template for students writing a bachelor or master thesis.

## Quick start

1. Open this repository in VSCode with the *Dev Containers* extension and re-open in container —
   the devcontainer ships with TeX Live, latexmk, the LTeX grammar/spell checker and an inline PDF viewer.
2. Edit [`settings.tex`](settings.tex) — title, author, supervisor, date.
3. Write your chapters in [`chapters/`](chapters/) and your bibliography in [`literature/literature.bib`](literature/literature.bib).
4. Save any `.tex` file — the container builds the PDF automatically.

## Repository layout

| Path | Purpose |
|---|---|
| [`thesis.tex`](thesis.tex) | Main entry point. Lists which chapters are included. |
| [`settings.tex`](settings.tex) | All thesis-specific values (edit this). |
| [`template/`](template/) | Title page, declarations, lists, bibliography. **Do not edit unless you know what you are doing.** |
| [`chapters/`](chapters/) | One file per chapter, plus `abstract.tex`. |
| [`glossary/glossary.tex`](glossary/glossary.tex) | Acronyms and glossary entries. |
| [`literature/literature.bib`](literature/literature.bib) | BibTeX bibliography. |
| [`forms/declaration.pdf`](forms/declaration.pdf) | Declaration of authorship (form of the Faculty of Computer Science), included as is. Fill it in and sign it after printing. |
| [`images/`](images/) | Logos and figures. |

## Building manually

```sh
latexmk -pdf thesis.tex
```

With older TeX Live versions, the `minted` package additionally needs `--shell-escape`.