## Week 7 — Issue selection

**Issue link:** [https://github.com/ascherj/pathreview/issues/151](https://github.com/ascherj/pathreview/issues/151)

**Issue title:** Bias detector patterns are too narrow to match common phrasings 

**Tier:** [✓] Tier 1  [ ] Tier 2  [ ] Tier 3

**Problem summary:**
The file `bias_detector.py` uses regex patterns to detect bias. This means that statements with the same sentiment but different word orderings would not be flagged for bias. We will likely have to rely on a different method of detection that does not require near-exact sentence matching. 

**Branch name:** `fix/151-bias-detector-too-narrow`

**Setup confirmation:** [✓] App runs locally at localhost:5173

**Cohort ledger:** [✓] Issue added to cohort ledger