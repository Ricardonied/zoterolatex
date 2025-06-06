# zoterolatex

This repository contains a small LaTeX document named `script` used to
compile and display bibliography entries exported from Zotero. It
leverages the `biblatex` package with `biber` as the backend to format
references in a custom style. Each entry prints the title, author,
abstract, optional keywords, and date. The entries are grouped by type
(e.g., articles, conference papers, theses, books).

## Requirements

- A LaTeX distribution (such as TeX Live)
- `biber` for processing `biblatex` references
- A `.bib` file exported from Zotero (UTF‑8 encoded)

## Usage

1. Export your references from Zotero to a `.bib` file and place it in
   this directory. The script expects a file named `zoterol.bib` by
default. Edit the `\addbibresource{}` line in `script` if your file has
another name.
2. Compile the document using `pdflatex` followed by `biber` and another
   `pdflatex` run, or use `latexmk` to automate the process:

   ```bash
   latexmk -pdf script
   ```

   The compilation will produce `script.pdf` containing a list of your
   references divided by entry type.

## Customization

The formatting of each reference is defined in `script` through
`\DeclareBibliographyDriver` commands. Adjust these commands if you need
to include additional fields or change the layout.
