# *Computational Mechanics* (Springer Nature, Journal ID 466) Submission Checklist

## 1. Manuscript Formatting & Compliance Summary

| Requirement (*Computational Mechanics* Guidelines) | Status | Implementation in Repository |
| :--- | :--- | :--- |
| **Template & Layout** (`sn-jnl.cls` with `[iicol]`) | Ready | `manuscript_final_v7.tex` uses `\documentclass[pdflatex,sn-basic,Numbered,iicol]{sn-jnl}` (`160 mm` two-column text block, `76 mm` column width, `8 mm` gutter). |
| **Scientific Content Unchanged** | Verified | Every physical equation, numerical value, theorem/derivation, discussion point, and conclusion preserved verbatim from `v7`. |
| **Abstract Length & Style** (150--250 words, self-contained) | Verified | **224 words**; zero citations, zero undefined abbreviations (`AR` defined at first mention). |
| **Indexing Keywords** (4--6 keywords) | Verified | **6 keywords**: *Strain-gradient elasticity; Bogner--Fox--Schmit finite element; Bloch--Floquet dispersion; Gradient micro-inertia; Wave steering; Phononic Bragg band gaps*. |
| **Heading Hierarchy** (Decimal, max 3 displayed levels) | Verified | Strict decimal hierarchy (`1` $\to$ `1.1` $\to$ `1.1.1` in main body; `Appendix A` $\to$ `A.1` in appendices); zero level-4 `\paragraph` displayed headings. |
| **Reference Style** (Square brackets `[1]`, `[1-3, 7]` + full DOIs) | Verified | `sn-basic` + `Numbered` options (`sn-basic.bst` included) format numbered square-bracket citations and `https://doi.org/...` links across all 52 cited references. |
| **Figures** (`Fig. 1`--`Fig. 13`, consecutive citation, caption rules) | Verified | All 13 two-panel vector PDFs (`W/H ≈ 2.0--2.15`) placed as two-column `figure*` (`\textwidth`), cited strictly `1` through `13`, with no terminal punctuation on captions. |
| **Tables** (`Table 1`--`Table 4`, consecutive citation, column fit) | Verified | `tab:case_params` placed at first callout in Sec. 3.3 so Tables 1--4 are cited strictly `1, 2, 3, 4`; Tables 1--2 (`table*`) and Tables 3--4 (`table` with native `\footnotetext`) sized cleanly for `[iicol]`. |
| **Two-Column Equation Wrapping** (`76 mm` column + equation tag) | Verified | `\setlength{\mathindent}{0pt}` set for `[iicol]` `[fleqn]` equations; multi-term equations in Secs. 2, 3, 4, 7 and Appendices A--B wrapped cleanly without changing any mathematical expression or `\label`. |
| **Statements & Declarations** (Mandatory Springer section) | Verified | Dedicated `\bmhead{Supplementary information}`, `\bmhead{Acknowledgements}` (HSHEC/HSRF written in full), and `\section*{Declarations}` (*Funding*, *Competing interests*, *Ethics approval*, *Data availability*, *Code availability*, *Author contributions*) before Appendices/References. |
| **Supplementary Material** (`Supplementary_Material.pdf`) | Verified | `Supplementary_Material.tex` formatted as a standalone `sn-jnl` file displaying article title, journal name (*Computational Mechanics*), author, affiliation, and corresponding email on Page 1; ready to attach directly in the portal's **Supplementary Material** upload option. |
| **Cover Letter** (Editor-in-Chief: Prof. Peter Wriggers) | Verified | `cover_letter.tex` formatted on clean single-page A4 academic letterhead addressed to Prof. Peter Wriggers, highlighting the $C^1$ BFS Bloch--Floquet formulation, Case-C mesh-refinement transparency (`0.552`--`0.565` decrement ratios), accompanying Supplementary Material attachment, and companion disclosure (`FINEL-D-26-00692R1`). |

---

## 2. Local / Overleaf Compilation Steps

1. **Main Manuscript (`manuscript_final_v7.pdf`)**:
   ```bash
   pdflatex manuscript_final_v7.tex
   bibtex manuscript_final_v7
   pdflatex manuscript_final_v7.tex
   pdflatex manuscript_final_v7.tex
   ```
2. **Supplementary Material (`Supplementary_Material.pdf`)**:
   ```bash
   pdflatex Supplementary_Material.tex
   bibtex Supplementary_Material
   pdflatex Supplementary_Material.tex
   pdflatex Supplementary_Material.tex
   ```
3. **Cover Letter (`cover_letter.pdf`)**:
   ```bash
   pdflatex cover_letter.tex
   ```

---

## 3. Springer Nature Portal (SNAPP) Upload Checklist

- **Portal URL**: Submit via the *Computational Mechanics* page on Springer Link (`https://link.springer.com/journal/466` $\to$ *Submit manuscript*).
- **Article Type**: *Original Article* / *Research*.
- **Author Metadata**:
  - **Corresponding Author**: Vipin Gupta (`vipin@gurugramuniversity.ac.in`)
  - **Affiliation**: Department of Mathematics, Gurugram University, Gurugram 122505, Haryana, India
  - **ORCID iD**: `0000-0002-5238-1963` (verify/link via ORCID button in SNAPP)
- **Files to Upload**:
  1. **Manuscript PDF** (`manuscript_final_v7.pdf`) + **LaTeX Source Package** (`manuscript_final_v7.tex`, `sn-jnl.cls`, `sn-basic.bst`, `references_final_v7.bib`, `sections/*.tex`, `tables/*.tex`, `figures/*.pdf`).
  2. **Supplementary Material**: Attach compiled `Supplementary_Material.pdf` directly in the portal's **Supplementary Material** file slot (description: *"Supplementary Material: Complete parameter summary, extended transfer-matrix comparisons and validation limits, expanded numerical consistency and mesh-convergence diagnostics, and Case-C gap-resolution data"*).
  3. **Cover Letter**: Upload `cover_letter.pdf`.
- **Publishing Model ($0 APC Hybrid Option)**:
  - *Computational Mechanics* is a **Hybrid (Transformative) Journal**. No APC choice is charged at submission; upon acceptance, select **Subscription / Traditional Publishing ($0 APC)** unless you have separate Open Choice funding.
- **Funding Entry in SNAPP**:
  - Funder: *Haryana State Higher Education Council (HSHEC), Government of Haryana*
  - Grant / Award Number: *14/66-2026 SPD/HSHEC/HSRF-38*
