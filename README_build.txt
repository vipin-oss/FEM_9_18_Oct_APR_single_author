Applied Physics Reviews — single-author source package

Contents
- manuscript_final_v7.tex: main AIP REVTeX 4.2 manuscript
- Supplementary_Material.tex: separately compiled supplementary material
- cover_letter.tex: APR cover letter source
- references_final_v7.bib, figures/, sections/, tables/, supplementary/tables/: required source dependencies
- alt_text_for_revision.txt and APR_submission_checklist.md: accessibility and submission notes

Build with TeX Live (REVTeX 4.2 and AIP bibliography style aipnum4-2):
  latexmk -pdf -halt-on-error -interaction=nonstopmode manuscript_final_v7.tex
  latexmk -pdf -halt-on-error -interaction=nonstopmode Supplementary_Material.tex
  latexmk -pdf -halt-on-error -interaction=nonstopmode cover_letter.tex

AIP uses the generic REVTeX class option `aip`; there is no separate `apr` class option.

Verification: GitHub Actions runs 39101209159 and 39101401210 both completed successfully with TeX Live 2025. Run 39101401210 compiled all three documents and uploaded the `apr-submission-pdfs` artifact.
Build and PDF artifact: https://github.com/vipin-oss/FEM_9_JSV/actions/runs/39101401210

Before submission, verify the CRediT roles, declarations, affiliation and contact details, and funding acknowledgment described in APR_submission_checklist.md.
