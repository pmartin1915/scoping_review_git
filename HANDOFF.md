# Session Handoff — Scoping Review Corrections

**Date:** February 27, 2026
**Git:** https://github.com/pmartin1915/scoping_review_git.git
**Next instance task:** Verify and execute remaining manual corrections to the scoping review manuscript.

---

## What's Done

### Automated Corrections (all verified PASS):
- **Table 1** (main manuscript): All 17 rows corrected — 38 cell changes (N values, methods, software)
- **Body text**: 19 targeted replacements (percentages, counts, ranges, study numbers)
- **Table S1** (Supplementary 4): Fully rebuilt with corrected 28-study list, 6 phantom studies removed, 6 real studies added
- **Master CSV**: Ground truth at `C:\Volumetric-tool\OPG_Scoping_Review\05_Synthesis\evidence_tables\01_Methods_Matrix_CORRECTED.csv`

### Corrected files:
- `Martin_OPG_Volumetric_Review_CORRECTED.docx` — Table 1 + body text fixed
- `Supplementary_4_Included_Studies_Table.docx` — Table S1 rebuilt (backup at `_BACKUP.docx`)
- `Martin_OPG_Volumetric_Review_BACKUP.docx` — untouched original

---

## What Remains (documented in MANUAL_CORRECTION_GUIDE.md)

### 1. Reference List (MUST FIX)
**Remove** (phantom studies, not cited in body text):
- Ref 14: Fouladi M, et al. Neurology. 2003 — phantom, never extracted
- Ref 15: Fisher MJ, et al. Neuro Oncol. 2012 — phantom, never extracted

**Check before removing:**
- Ref 3: Avery RA, et al. JAMA Ophthalmol. 2014 — NOT cited in body text per scan

**Keep** (confirmed cited):
- Ref 1: Listernick 2007 — background, cited [1]
- Ref 2: Avery 2011 — background, cited [1,2] in intro
- Ref 6: Avery VA testing — cited [6] in discussion

**Add** (studies in the review but missing from references):
- Millward CP, et al. Childs Nerv Syst. 2015;31(11):2055-62.
- Calixto EL, et al. Childs Nerv Syst. 2019;35(1):63-72.
- Liu Z, et al. Neurosurg Rev. 2022;45(3):2277-87.
- Diaz RJ, et al. Childs Nerv Syst. 2008;24(6):707-12.

**Then:** Renumber ALL [N] citations throughout the entire document.

### 2. Software Lists in Method Paragraphs
**Para 46 (Manual segmentation):**
- Current: "open-source platforms (3D Slicer, ITK-SNAP, Horos, FSL) or commercial software (BrainLab, Analyze)"
- Remove: FSL, BrainLab, Analyze (these are semi-auto, not manual)
- Add: MNI-DISPLAY, Eclipse TPS
- Suggested: "open-source platforms (3D Slicer, ITK-SNAP, Horos, MNI-DISPLAY) or commercial software (Eclipse TPS)"

### 3. Geographic Percentages (Para 43)
Current: "North America (50%), Europe (28%), Middle East (11%), Asia (7%), South America (4%)"
- 5 North American phantoms removed, replaced by: 1 North American (Diaz), 1 European (Millward), 1 Asian (Liu), 1 South American (Calixto)
- Needs recalculation from the 28 corrected studies

### 4. Population Percentages (Para 43)
Current: "NF1-associated OPG (29%), sporadic OPG (4%), and mixed (68%)"
- May have shifted with study list change. Verify against corrected CSV.

### 5. Timeline Paragraph (Para 51)
Current: "approximation methods predominated 2008–2013"
- Earliest approximation study is now Kelly 2012 (not 2008 — Diaz 2008 is linear, not approximation)
- Consider: "2012–2013" or rephrase

### 6. File Replacement
- `_CORRECTED.docx` needs to replace the original `.docx` (original was locked during script execution because it was open in Word)

---

## Key Reference Files

| File | Location | Purpose |
|------|----------|---------|
| Corrected manuscript | `C:\Scoping Review Final\Martin_OPG_Volumetric_Review_CORRECTED.docx` | Working file for remaining edits |
| Corrected Supplementary 4 | `C:\Scoping Review Final\Supplementary_4_Included_Studies_Table.docx` | Table S1 — DONE |
| Manual correction guide | `C:\Scoping Review Final\MANUAL_CORRECTION_GUIDE.md` | Full details on remaining work |
| Master CSV (ground truth) | `C:\Volumetric-tool\OPG_Scoping_Review\05_Synthesis\evidence_tables\01_Methods_Matrix_CORRECTED.csv` | PDF-verified data for all 28 studies |
| Audit report | `c:\opg-segmentation\docs\reference\scoping_review_audit_feb26.md` | Complete findings from PDF audit |
| Source PDFs | `C:\Volumetric-tool\OPG_Scoping_Review\02_PDFs\` | 29 files across 7 thematic batches |
| Extraction database | `C:\Volumetric-tool\OPG_Scoping_Review\03_Extractions\_EXTRACTION_STATUS.csv` | Original extraction tracking |
| Reference list CSV | `C:\Volumetric-tool\OPG_Scoping_Review\05_Synthesis\evidence_tables\06_Reference_List_Updated.csv` | DOIs and PMIDs |

---

## Verification Checklist (run after all corrections)

- [ ] Ctrl+F "292" — should not appear (old Kilian N)
- [ ] Ctrl+F "Fouladi" — should be removed
- [ ] Ctrl+F "Fisher MJ" — ref 15 should be removed
- [ ] Ctrl+F "179" — should not appear
- [ ] Ctrl+F "n=30" — should only appear as "n=14-38"
- [ ] Count references — should be ~31 (30 - 2 removed + 4 added - Avery 2014 TBD)
- [ ] Verify every [N] citation points to correct reference after renumbering
- [ ] Table 1 matches Table S1 for the 17 shared studies
- [ ] Geographic and population percentages add to ~100%
- [ ] Generate final PDF for resubmission

---

## Context for Next Instance

- **Perry disclosed LLM use in the manuscript** — this is already in the published submission
- **JNOD editor said** "incorporate changes in future revisions" — no urgency, corrections go in with reviewer response
- **All clinical findings are correct** — every ICC, kappa, Dice, threshold, correlation verified against source PDFs
- **The errors are metadata only** — sample sizes, software names, method categories
- **6 phantom studies** were AI hallucinations during compilation from extraction database to manuscript tables. The extraction database itself is correct.
- **Perry cannot annotate scans himself** — he's a DNP-FNP student, not a radiologist. This is addressed in the project timeline.
- **Use PyPDF2 for reading PDFs on Windows:** `PYTHONIOENCODING=utf-8 "/c/Users/perry/AppData/Local/Programs/Python/Python313/python.exe"` with `from PyPDF2 import PdfReader`
- **Use python-docx for Word docs:** Same Python path, `from docx import Document`
