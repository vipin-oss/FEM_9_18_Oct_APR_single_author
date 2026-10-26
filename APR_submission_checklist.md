# Applied Physics Reviews submission checklist

## Prepared in this repository

- `manuscript_final_v7.tex` — converted to the generic AIP REVTeX 4.2 (`aip`, `preprint`) submission format and set to the single author Vipin Gupta.
- `Supplementary_Material.tex` — standalone AIP-style supplementary document, also carrying only Vipin Gupta as author; compile and upload its PDF separately.
- `cover_letter.tex` — APR-specific Original Research letter addressing the knowledge gap, novelty, importance, broad readership, and related work, rewritten for one author.
- `alt_text_for_revision.txt` — numbered alt text for all main-paper figures and tables. AIP requests a separate `.txt` or `.docx` file upon revision; supplementary-table alt text appears below the captions in `Supplementary_Material.tex`.
- `APR_submission_checklist.md` — build notes and author-submission checks.

The corresponding author confirmed that there is no closely related work to list, that the sole author has no competing interests, and that the manuscript is original and not under consideration elsewhere. The cover letter now uses a sole-author approval statement.

The existing `highlights.tex` is not part of the required APR package based on the AIP instructions checked for this preparation. Do not upload it unless the submission portal specifically requests it. AIP recommends a separate highlight image with a revised submission; this is different from textual highlights.

## Author details and CRediT roles

The manuscript identifies Vipin Gupta as the sole author. A CRediT draft is included for Vipin Gupta (Conceptualization, Methodology, Software, Validation, Formal analysis, Investigation, Data curation, Writing – original draft, Writing – review and editing, Visualization, and Funding acquisition). Verify that each listed role accurately reflects the work and remove any role that does not apply.

Also verify the name, affiliation, email address, HSHEC/HSRF acknowledgment and sanction-letter number, and that the Data Availability Statement accurately describes the materials supplied.

## Build and upload sequence

Use a LaTeX installation containing REVTeX 4.2 and the AIP BibTeX style `aipnum4-2` (or upload the sources to AIP's official Overleaf template):

```sh
latexmk -pdf -bibtex -interaction=nonstopmode manuscript_final_v7.tex
latexmk -pdf -bibtex -interaction=nonstopmode Supplementary_Material.tex
pdflatex -interaction=nonstopmode 'cover_letter.tex'
```

Review the logs for missing citations/references, confirm all figures appear in the main PDF, and check pagination, tables, graphics quality, and bibliography. Upload the single compiled main-manuscript PDF plus the separate supplementary-material PDF. Upload the cover letter in the format requested by the portal. Keep the `.tex`, `.bib`, and figure files available if the system requests editable source files.

A static pass confirmed balanced braces and environments, resolved internal references, present bibliography keys, and existing figure files. No LaTeX engine is installed in this workspace. GitHub Actions run [39101401210](https://github.com/vipin-oss/FEM_9_JSV/actions/runs/39101401210) completed successfully with TeX Live, compiling the manuscript, supplement, and cover letter and uploading the PDFs as the `apr-submission-pdfs` artifact. Download the PDFs from that run's Artifacts section; after any source changes, verify the newest run as well. The workflow and sources are kept in this repository for repeatable builds.

## Relevant AIP instructions

- [AIP Publishing author instructions](https://publishing.aip.org/resources/researchers/author-instructions/)
- [Applied Physics Reviews policies](https://pubs.aip.org/aip/apr/pages/policies)
- [Official AIP/Overleaf LaTeX template](https://www.overleaf.com/latex/templates/template-for-submission-to-aip-journals/wdmsvzfjgvyj)
