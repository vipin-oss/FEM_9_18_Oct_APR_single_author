Computational Mechanics (Springer Nature) LaTeX Build Notes
===========================================================

Main manuscript (`manuscript_final_v7.tex`)
-------------------------------------------
Class & style files (included in repository root):
  - `sn-jnl.cls`          : Official Springer Nature journal class, invoked with
                            `\documentclass[pdflatex,sn-basic,Numbered,iicol]{sn-jnl}`
                            (`[iicol]` = Computational Mechanics two-column layout;
                             `[sn-basic,Numbered]` = `[1]`, `[1-3, 7]` numbered citations
                             with full `https://doi.org/...` links).
  - `sn-basic.bst`        : Official Springer Nature BibTeX style used by `sn-basic`.
  - `sn-mathphys-num.bst` : Retained alongside `sn-basic.bst` for standard Springer
                            Nature template completeness.

Compile commands:
  pdflatex manuscript_final_v7.tex
  bibtex manuscript_final_v7
  pdflatex manuscript_final_v7.tex
  pdflatex manuscript_final_v7.tex

Or with `latexmk`:
  latexmk -pdf manuscript_final_v7.tex

Supplementary Material (`Supplementary_Material.tex` -> `Supplementary_Material.pdf`)
-------------------------------------------------------------------------------------
Compiled separately as a standalone Springer Nature single-column supplement to
be attached directly in the portal's Supplementary Material upload option:
  pdflatex Supplementary_Material.tex
  bibtex Supplementary_Material
  pdflatex Supplementary_Material.tex
  pdflatex Supplementary_Material.tex

Note: `Supplementary_Material.tex` uses `tabularray` (`longtblr`) for Table S1,
requiring TeX Live 2022 or newer (or current MiKTeX / Overleaf).

Cover letter (`cover_letter.tex`)
---------------------------------
Addressed to Prof. Peter Wriggers, Editor-in-Chief, Computational Mechanics:
  pdflatex cover_letter.tex

Portal upload notes for Springer Nature (SNAPP)
-----------------------------------------------
- Upload editable LaTeX source files (`manuscript_final_v7.tex`, `sn-jnl.cls`,
  `sn-basic.bst`, `references_final_v7.bib`, `sections/*.tex`, `tables/*.tex`,
  and `figures/*.pdf`) plus the compiled `manuscript_final_v7.pdf`.
- Upload `Supplementary_Material.pdf` directly in the portal's Supplementary
  Material attachment slot alongside the manuscript.
- Upload `cover_letter.pdf` as Cover Letter.
- Publishing model: Computational Mechanics (Journal ID 466) is a transformative
  hybrid journal; select subscription / traditional publishing ($0 APC) upon
  acceptance if Open Choice OA is not required.
