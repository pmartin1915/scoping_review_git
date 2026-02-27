# Manual Correction Guide — Martin OPG Volumetric Review

**Date:** February 26, 2026
**Status:** Automated corrections completed. Items below require manual editing in Word.

**Files:**
- Corrected manuscript: `Martin_OPG_Volumetric_Review_CORRECTED.docx`
- Corrected Supplementary 4: `Supplementary_4_Included_Studies_Table.docx`
- Backup: `Martin_OPG_Volumetric_Review_BACKUP.docx`

---

## What's Already Fixed (Automated)

### Table 1 — All 17 rows corrected:
- All N values (38 cell changes)
- Method categories: Avery 2018, Avery 2023 (Manual→Semi-auto), Kilian (Semi-auto→Manual), Bennebroek 2024 (Manual→Approx), D'Arco (Manual→Semi-auto), Maloney (Manual→Approx), Yeom (Manual→Approx)
- Software: Alshowaeir (ITK-SNAP→ABC/2), Gorodezki (ITK-SNAP→BrainLab Elements), D'Arco (Horos→OsiriX MD), Kilian (BrainLab→Horos), Kelly 2012 (N/A→ITK-SNAP), Yeom (Custom→Functool)
- Reliability: Yeom (ICC 0.998→ICC 0.998-1.000)

### Body Text — 19 changes:
- n=30-42 → n=14-38
- Twenty-seven → Twenty-six studies
- Method percentages: 44%→31%, 33%→35%, 7%→8%, 15%→27%
- Method counts: n=12→8 (manual), n=4→7 (approx)
- "One study 2D" → "Two studies linear or 2D"
- "Among 27 studies" → "Among 26 studies"
- Year range: 2003-2025 → 2008-2025
- Publication stat: 68% (n=19) → 75% (n=21)
- Sample size range: 15-292 → 3-186
- Alshowaeir n=17 → n=16
- Limitations: 2 of 27 → 2 of 26

---

## MUST FIX: Reference List Changes

### Remove these references (phantom studies — not cited in body text):
| Current Ref # | Citation | Reason |
|---|---|---|
| 14 | Fouladi M, et al. Neurology. 2003 | Phantom — never extracted, not cited in text |
| 15 | Fisher MJ, et al. Neuro Oncol. 2012 | Phantom — never extracted, not cited in text |

### Check before removing (may be legitimate background citations):
| Current Ref # | Citation | Status |
|---|---|---|
| 3 | Avery RA, et al. JAMA Ophthalmol. 2014 | NOT cited in body text per scan. Remove unless you deliberately use it for background. |

### Keep (confirmed cited in body text):
| Current Ref # | Citation | Where cited |
|---|---|---|
| 1 | Listernick 2007 | Background [1] |
| 2 | Avery 2011 (J Neuroophthalmol) | Introduction [1,2] — review article, background |
| 6 | Avery (VA testing feasibility) | Discussion [6] — still cited |

### Add these references (studies now in the review but missing from reference list):
| Study | Full Citation |
|---|---|
| Millward 2015 | Millward CP, Perez da Rosa S, Avula S, et al. The role of early intra-operative MRI in partial resection of optic pathway/hypothalamic gliomas in children. Childs Nerv Syst. 2015;31(11):2055-62. |
| Calixto 2019 | Calixto EL, Ono SE, Teixeira BCAT, et al. Monitoring optochiasmatic-hypothalamic glioma volumetric changes by MRI in children under clinical surveillance or chemotherapy. Childs Nerv Syst. 2019;35(1):63-72. |
| Liu 2022 | Liu Z, Ding Z, Zhang J, et al. The role of imaging features and resection status in the survival outcome of sporadic optic pathway glioma children. Neurosurg Rev. 2022;45(3):2277-87. |
| Diaz 2008 | Diaz RJ, Laughlin S, Nicolin G, Bouffet E. Assessment of chemotherapeutic response in children with proptosis due to optic nerve glioma. Childs Nerv Syst. 2008;24(6):707-12. |

### After adding/removing: Renumber ALL citations
This will cascade through the entire document. Every [N] bracket in the text needs to be updated.

**Suggested approach:** Do this in Word using Find & Replace carefully, working from highest ref number to lowest to avoid double-replacement.

---

## SHOULD FIX: Software Lists in Method Descriptions

### Para 46 (Manual segmentation):
**Current:** "open-source platforms (3D Slicer, ITK-SNAP, Horos, FSL) or commercial software (BrainLab, Analyze)"

**Corrected list of software used by manual studies:**
- Avery 2016b: Custom
- Avery 2016a: ITK-SNAP
- Bennebroek 2024a: 3D Slicer
- Liu 2022: 3D Slicer
- Kilian 2022: Horos
- Calixto 2019: MNI-DISPLAY
- Lambron 2016: NR
- Youn 2022: Eclipse TPS

**Suggested:** "open-source platforms (3D Slicer, ITK-SNAP, Horos, MNI-DISPLAY) or commercial software (Eclipse TPS)"
- Remove: FSL (semi-auto, not manual), BrainLab (semi-auto, not manual), Analyze (semi-auto, not manual)
- Add: MNI-DISPLAY, Eclipse TPS

### Para 47 (Semi-automated):
Software used by semi-auto studies: Analyze 9.0+SPM, ABC/2, MRIcron, Analyze+SPM, Custom algorithm, OsiriX MD, FSL+Fiji, Custom DL+manual, BrainLab Elements

---

## SHOULD CHECK: Geographic Percentages

Para 43 currently says: "North America (50%), Europe (28%), Middle East (11%), Asia (7%), and South America (4%)"

With 6 phantom studies out and 6 real studies in, these percentages may have shifted. Quick count needed:
- Classify each of the 28 corrected studies by region
- Recalculate percentages

The new studies added:
- Millward 2015: UK (Europe)
- Calixto 2019: Brazil (South America)
- Liu 2022: China (Asia)
- Diaz 2008: Canada (North America)

The phantom studies removed:
- Avery 2011: USA (North America)
- Avery 2014: USA (North America)
- Avery 2017: USA (North America)
- Wright 2019: Unknown
- Fouladi 2003: USA (North America)
- Fisher 2021: USA (North America)

**Net effect:** Removed 5 North American, added 1 North American, 1 European, 1 Asian, 1 South American. Percentages will shift toward more international distribution.

---

## SHOULD CHECK: Timeline Paragraph (Para 51)

**Current:** "approximation methods predominated 2008–2013, semi-automated approaches emerged 2014–2018"

With corrected study list:
- Earliest approximation: Kelly 2012 (not 2008)
- Diaz 2008 is linear (not approximation)
- Consider updating to "2012-2013" or just "early studies"

---

## SHOULD CHECK: Population Percentages (Para 43)

**Current:** "NF1-associated OPG (29%), sporadic OPG (4%), and mixed (68%)"

These percentages may have shifted with the study list change. Verify against the 28 corrected studies.

---

## OPTIONAL: Disambiguation of Duplicate Authors

The corrected Table S1 uses "2024a" and "2024b" suffixes for the two Bennebroek papers and "2016a"/"2016b" for the two Avery 2016 papers. Table 1 in the main manuscript only shows one of each, so suffixes aren't strictly needed there. However, for consistency with Supplementary 4, consider adding:
- Table 1: "Avery (2016)" could become "Avery (2016b)" since it's the volume-RNFL paper
- Table 1: "Bennebroek (2024)" could become "Bennebroek (2024b)" since it's the ICC paper

---

## Verification Checklist

After making ALL corrections (automated + manual):

- [ ] Ctrl+F "292" — should only appear if quoting another source
- [ ] Ctrl+F "Fouladi" — should be removed entirely (unless kept as background)
- [ ] Ctrl+F "Fisher MJ" — should be removed (ref 15)
- [ ] Ctrl+F "179" — should not appear
- [ ] Ctrl+F "n=30" — should only appear as "n=14-38"
- [ ] Count references — should be ~31 (current 30 - 2 removed + 4 added - Avery 2014 TBD)
- [ ] Verify every [N] citation points to the correct reference
- [ ] Verify Table 1 matches Supplementary Table S1 for the 17 shared studies
- [ ] Re-read Discussion paragraph on thresholds (uses corrected n=14-38)
