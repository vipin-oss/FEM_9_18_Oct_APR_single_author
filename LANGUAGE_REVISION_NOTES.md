# Language Revision Notes (Hinglish)

Paper: "Directional Wave Dispersion and Energy-Flow Steering in Two-Dimensional Strain-Gradient Elastic Solids" (IJES).
Sirf wording badli gayi hai. Koi number, equation, table entry, figure, label, \cite, \ref ya \eqref change nahi hua.
Script check (backup ke against): saare \cite keys, \ref/\eqref, \label aur numbers ka multiset before/after bilkul identical hai (main + sections + tables).

## Section-wise kya badla

**Abstract** — Active voice mein likha ("We use / We specify / We solve"). Equation hata kar "2.78 degrees" likha (abstract mein math nahi chahiye tha). Aakhri lamba sentence toda. Ab 165 words, "This paper studies ..." se shuru, koi equation ya citation nahi.

**Sec 1 (Introduction)** — Flow wahi hai: background, literature, gap, objectives. "then ... then" repetition hataya. "followed" (do baar aaya tha) ko "then reported" / "came later" mein vary kiya. "bring in" → "include". Colon wali listing sentences ko simple sentences mein toda. "It is the characteristic-length tensor that rotates" ko seedha "The characteristic-length tensor rotates" kiya. Semicolon wala limit sentence do sentences mein split. "optimisation/discretisation/homogenised" British spelling.

**Sec 2 (Continuum)** — "It does not use ..." ko "rather than ..." mein merge kiya. Active voice ("We keep the ellipse area fixed ...", "we decompose ..."). "retain" → "keep", "yields" → "gives". "parameterized" → "parameterised". Semicolons full stop mein convert. "reverses the off-diagonal component" → "reverses the sign of ..." (zyada saaf).

**Sec 3 (Bloch)** — Passive → active: "We repeat the square cell ...", "we order the eigenfrequencies ...", "We measure ...", "We evaluate the angular derivative ...". Heading "Nondimensionalization" → "Nondimensionalisation". Leg-gap item ka semicolon split. Fig 2 caption mein full stop add.

**Sec 4 (FEM)** — BFS wali line ko intro se alag wording di (same matlab). "Their Bloch-phase mapping is shown in Figure" → "Figure shows ...". "$8n^2$ counts the independent degrees of freedom ..." ka repetition ghataya (math token $8n^2$ dono jagah preserve kiya). "via" → "through". Quadrature para ka semicolon split. "Elements intersected by the inclusion are integrated ..." → active "we use sub-cell Gauss sampling ...". "generalized/nonnegative" → "generalised/non-negative". "is halved" → "we halve"; "Band gaps are computed" → "We compute".

**Sec 5 (Verification)** — "The implementation is checked" → "We check the implementation". "analyze" → "analyse", "normalized/normalization" → "normalised/normalisation". Semicolon split ("... data are unavailable. We do not infer a percentage error ..."). "Mesh convergence is tested" → "We test mesh convergence". "gives ... gives" repetition: Figure ke liye "shows". "The $32^2$ result is excluded" → "We exclude the $32^2$ result". "exceeds the floor by approximately 3×10^7" → "by a factor of approximately 3×10^7" (ratio hi matlab tha; number same).

**Sec 6 (Results)** — "its branches next to theirs" (confusing pronouns) → "the reference branches next to the anisotropic ones". "on the propagation direction" → "onto ...". Case-C para: semicolon split, "The ratio r0/L = ..." sentence banaya, interface integration active voice. Captions mein full stops add aur semicolon hataya. Steering para: "we sample directions ..." active; principal-direction semicolon split. Aakhri sentence: "are consistent with orientation shifting the lobes ..." → "these symmetries indicate that rotation shifts the lobes ..." (grammar smooth).

**Sec 7 (Micro-inertia)** — "its strain energy" (unclear antecedent) → "the strain energy". "The growing gradient-energy fraction reflects ..." → "This growth reflects ..." (repetition avoid). "analyzed" → "analysed" (2 jagah). "grows without bound" do baar tha; ek jagah "is unbounded" kiya.

**Sec 8 (Discussion)** — "optimized" → "optimised". "Other branches are not covered by this result" → "This result does not cover the other branches". Aakhri sentence active: "It does not include dissipation, nonlinear effects, ...". "polarization" → "polarisation".

**Sec 9 (Conclusions)** — "No complete band gap is found" → "We find no complete band gap". "normalized units" → "normalised units". "grows without bound" → "is unbounded" (sec 7 se same words repeat na ho).

**App A** — "yields" → "gives" (2 jagah). "Similarly, the group velocity ... is given by" → "The group velocity ... is". "attains" → "reaches". "analytical horizon" → "analytical limit" (baaki jagah "limit"/"asymptote" hi use hota hai; sirf equation labels mein "v_horizon" hai, wo internal hain, untouched). Aakhri "grow without bound" → "are ... unbounded" (intro se repetition avoid).

**App B** — "are derived here" → "We derive". "is expressed by the continuity relation" → "takes the continuity form". Dangling participle fix: "Integrating over the unit cell, the flux ... satisfy" → "After integration over the unit cell, ... satisfy". Lamba residual sentence do active sentences mein split ("We obtain it from ... . The cycle-averaged flux ... is compared with ...").

**App C** — "Algebraic checks are reported separately" → "We report ...". "are given in Table" → "Table ... gives". "normalized/normalization/discretization" → British forms. "which yields 126 gap-measure values" wala lamba sentence do sentences mein split. "since" → "because" (ek jagah). "FE mesh" → "finite-element mesh" (abbreviation sirf wahan tha). "better resolved" → "better-resolved". Semicolons split. Captions mein full stop.

**Tables** — tab08 mein sirf spelling: "normalization" → "normalisation", "normalized" → "normalised" (2×), "These yield" → "These give". Koi data entry nahi badli. Baaki table bodies untouched.

## Scientifically unclear sentences (chhoda, fix nahi kiya)

1. **Sec 5**: "The floor for successive-mesh changes is ε_Δ = 4.63×10⁻¹¹, which differs from the eigensolver reproducibility." — kis number se differ karta hai, yeh sentence mein clear nahi (app C mein "distinct from eigensolver reproducibility at the finest level" se thoda context milta hai).
2. **Sec 6**: "The deviation field is headless-periodic and mirror co-symmetric" — "headless-periodic" term paper mein defined nahi hai; shayad π-periodic (direction without arrow) matlab hai, par sure nahi.
3. **App C bullet 5**: "the bounded phase-speed result differs from its asymptote by 2.85×10⁻⁴" — Sec 7 ke 0.3163 vs 0.3162 se absolute difference 1×10⁻⁴ aata hai; 2.85×10⁻⁴ ka basis (absolute/relative, underlying digits) text se verify nahi hota.
4. **Sec 3(a)**: "Δ_GX denotes the Γ–X leg" — asal mein wo us leg par ka leg-gap measure denote karta hai, leg ko nahi. Original wording ka hi matlab tha, isliye aise hi rakha.

## Number/notation inconsistencies (report only, fix nahi kiya)

1. **Δ subscripts**: $\Delta_{GX}$, $\Delta_{XM}$, $\Delta_{MG}$ mein "G" = Γ hai, jabki prose mein Γ–X likha hai. Minor notation mismatch.
2. **Wavenumber ring**: text mein $|\mathbf{k}| = \bar{k} = 0.5$ (bold magnitude aur barred scalar mix), captions mein kabhi $|\mathbf{k}|=0.5$, kabhi $\bar{k}=0.5$. Ek hi quantity ke teen likhne ke tareeke.
3. **Case-C period**: text mein $L$, Figure 7 mein $a$ (paper khud isko note karta hai Sec 6.6 mein — jaankari ke liye list kiya).
4. **"2D" vs "two-dimensional"**: Sec 2 mein "Under plane strain in 2D" rakha gaya hai kyunki numbers-identical verification ka hissa hai; baaki jagah "two-dimensional" likha hai.
5. **p = 4.17, CI [3.15, 5.20]** Sec 5 aur App C mein consistent; **42 = 6×7** configuration count consistent; **0.03%** (Sec 7/App A) ke saath 0.3163 vs 0.3162 consistent (≈0.032%).
6. Main file ke comment mein "double-anonymized" (American spelling) hai — wo sirf comment hai, PDF mein print nahi hota, isliye chhoda.

## Compile note

Is sandbox mein TeX engine available nahi hai (pdflatex/tectonic install nahi ho paya). Isliye pdflatex+bibtex run karke PDF check karna **local machine par** karna hoga. Saare edits exact-string prose changes hain; brace/environment balance aur cite/ref/label/number multisets script se verify ho chuke hain — compile issues ka risk bahut kam hai, par final PDF check zaroor karein.
