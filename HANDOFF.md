# Scoping Review Corrections — Verification Handoff

**Date:** 2026-03-02
**From:** Claude Code (Opus 4.6) audit session
**To:** Next instance — please double-check our work
**Repo:** https://github.com/pmartin1915/scoping_review_git.git
**Branch:** main

---

## What Happened This Session

Perry's scoping review manuscript (submitted to JNOD — Journal of Neuro-Oncology Discovery) had systematic errors from LLM-generated content. Prior sessions applied bulk corrections. This session performed a comprehensive audit of those corrections and applied 5 additional fixes.

### Commits This Session

| Commit | Description |
|--------|-------------|
| `24afeb6` | Fix cross-table consistency and citation errors (5 targeted fixes) |
| `4450708` | Update population percentages to match S1 classifications (Perry's manual edit) |

### Prior Correction Commits (from earlier sessions)

| Commit | Description |
|--------|-------------|
| `d0b07c1` | Fix geographic percentages to match Supplementary Table S1 |
| `b4a219c` | Complete remaining corrections: reference list, citations, software, geography |
| `a405ba6` | Add corrected manuscript and manual correction guide |
| `32e7c61` | Original submission files (as submitted to JNOD) |

---

## Fixes Applied in `24afeb6`

1. **Maloney 2021 method label (S1):** Changed "Manual" to "Approximation" in Supplementary_4 Table S1, row 20, col 6. Matches Table 1 ("Approx") and body text categorization.

2. **Kelly 2012 software (S1):** Changed "N/A" to "ITK-SNAP" in Supplementary_4 Table S1, row 14, col 7. Matches Table 1 and CSV ground truth.

3. **FSL in Discussion (main manuscript):** Replaced "FSL" with "MNI-DISPLAY" in Para 80 discussion of free software platforms. Now matches Para 46 Methods section list.

4. **Nalepa citation added (main manuscript):** Changed "[16]" to "[16,26]" in Para 72 where automated/deep learning methods are discussed. Nalepa [26] is one of only 2 automated studies (alongside Jiang [16]) and was previously uncited in body text.

5. **Bennebroek ICC citation fix (main manuscript):** Changed "ICC 0.96 [9]" to "ICC 0.96 [10]" in Para 53. [9]=Bennebroek 2024a (no reliability), [10]=Bennebroek 2024b (ICC 0.96). Pre-existing error preserved through citation remapping.

## Fix Applied in `4450708`

6. **Population percentages (main manuscript):** Perry manually updated body text from NF1=29%, sporadic=4%, mixed=68% to NF1=18%, sporadic=4%, mixed=79%. Now matches Supplementary Table S1 classifications.

---

## Key Files

| File | Location | Purpose |
|------|----------|---------|
| Main manuscript | `Martin_OPG_Volumetric_Review_CORRECTED.docx` | Corrected JNOD submission |
| Supplementary Table S1 | `Supplementary_4_Included_Studies_Table.docx` | 28 included studies |
| Ground truth CSV | `C:\Volumetric-tool\OPG_Scoping_Review\05_Synthesis\evidence_tables\01_Methods_Matrix_CORRECTED.csv` | PDF-verified reference data |
| Audit report | `C:\Users\perry\.claude\plans\hazy-orbiting-squid.md` | Full audit findings |
| Original submission | `Martin_OPG_Volumetric_Review.docx` | Pre-correction version |
| Backup | `Martin_OPG_Volumetric_Review_BACKUP.docx` | Clean copy before any script edits |

---

## Verification Checklist for Next Instance

### Priority 1: Verify the 6 fixes above

- [ ] **Maloney S1:** Open Supplementary_4, find Maloney 2021 row. Confirm method column says "Approximation" (not "Manual").
- [ ] **Kelly S1:** Same file, find Kelly 2012 row. Confirm software column says "ITK-SNAP" (not "N/A").
- [ ] **FSL→MNI-DISPLAY:** Open CORRECTED.docx, find Para 80 (Discussion, "free software platforms"). Confirm list includes "MNI-DISPLAY" not "FSL".
- [ ] **Nalepa [16,26]:** Find Para 72 (automated methods discussion). Confirm citation reads "[16,26]" not just "[16]".
- [ ] **Bennebroek ICC [10]:** Find Para 53 (reliability discussion). Confirm "ICC 0.96 [10]" not "[9]".
- [ ] **Population %:** Find Para 43 (study characteristics). Confirm NF1=18%, sporadic=4%, mixed=79%.

### Priority 2: Cross-reference integrity

- [ ] **Table 1 vs CSV:** All 17 rows match ground truth CSV (N values, methods, software, reliability).
- [ ] **Table S1 vs CSV:** All 28 study rows match CSV.
- [ ] **Table 1 vs S1 consistency:** Method categories agree for all overlapping studies. Note: Avery 2016 and Bennebroek 2024 have multiple sub-studies — Table 1 selectively includes specific ones (2016b, 2024b).

### Priority 3: Method count consistency

- [ ] Body text method breakdown sums to 26 volumetric studies: Manual=8 + Semi-auto=9 + Auto=2 + Approx=7 = 26.
- [ ] Percentages: 31% + 35% + 8% + 27% = 101% (rounding, acceptable).
- [ ] Total study count: 28 total = 26 volumetric + 2 non-volumetric (linear/2D).

### Priority 4: Citation integrity spot-checks

- [ ] [3] → Avery 2016b (RNFL prediction) in context of AVP >3.0 mL
- [ ] [6,7] → Avery 2023 + 2018 in context of AVP >1.75 mL
- [ ] [8] → Alshowaeir in context of rs=-0.939
- [ ] [10] → Bennebroek 2024b in context of ICC 0.96
- [ ] [15] → Gorodezki in TGV threshold context
- [ ] [16,26] → Jiang + Nalepa in deep learning context
- [ ] [17] → Kelly 2012 in volume-VA r=0.0 context
- [ ] All citations in range [1-31], no old numbers remaining

### Priority 5: Phantom/error scan

- [ ] No instances of: "292", "140", "179", "Fouladi", "Fisher MJ" (as first author), "Wright", "Avery 2014", "Avery 2011"
- [ ] No "n=30" without "n=14" nearby
- [ ] Reference list has exactly 31 entries, alphabetically ordered

### Priority 6: Geographic and timeline values

- [ ] Geographic: NA 43%, EU 36%, ME 11%, Asia 7%, SA 4% (or similar — verify against S1 countries)
- [ ] Timeline: "approximation methods predominated 2012-2013" (not 2008-2013)
- [ ] Sample range: "from 3 to 186" (not "15 to 292")
- [ ] Year range: "between 2008 and 2025" (not 2003)

---

## Known Accepted Items

These were reviewed and determined to be acceptable as-is:

- **Bennebroek 2024b (ref [10]) only cited once:** Now cited in Para 53 for ICC. Also appears in Table 1. Adequate.
- **Kelly software discrepancy:** Table 1 says "ITK-SNAP", S1 now also says "ITK-SNAP". CSV notes it was used for only 2 patients. Defensible.
- **Method % rounding to 101%:** Standard rounding behavior with 4 categories. Acceptable.

---

## Methodology Notes

- **Ground truth source:** `01_Methods_Matrix_CORRECTED.csv` — PDF-verified by Perry against original study publications
- **Audit tools used:** Parallel sonnet/haiku subagents for data extraction, Gemini 3 Pro Preview (via MCP PAL codereview) for expert validation
- **Correction scripts:** 4 Python scripts (fix_manuscript.py through fix_remaining_corrections.py) using python-docx for Word manipulation. Scripts preserved in repo for reproducibility.
- **JNOD response to errors:** "Incorporate changes in future revisions" — no urgency, but corrections applied proactively
