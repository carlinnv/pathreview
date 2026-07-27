## Week 7 — Issue selection

**Issue link:** [https://github.com/ascherj/pathreview/issues/151](https://github.com/ascherj/pathreview/issues/151)

**Issue title:** Bias detector patterns are too narrow to match common phrasings 

**Tier:** [✓] Tier 1  [ ] Tier 2  [ ] Tier 3

**Problem summary:**
The file `bias_detector.py` uses regex patterns to detect bias. This means that statements with the same sentiment but different word orderings would not be flagged for bias. We will likely have to rely on a different method of detection that does not require near-exact sentence matching. 

**Branch name:** `fix/151-bias-detector-too-narrow`

**Setup confirmation:** [✓] App runs locally at localhost:5173

**Cohort ledger:** [✓] Issue added to cohort ledger



## Week 8 — Reproduction & solution planning

**Reproduction commit link:** [https://github.com/carlinnv/pathreview/tree/fix/151-bias-detector-too-narrow](https://github.com/carlinnv/pathreview/tree/fix/151-bias-detector-too-narrow)

**Reproduction summary:**
I reproduced the issue by running the test suite. I found that 9 out of the 32 tests passed. The ones that failed typically failed because the regex used to detect biased sentences were too rigid to capture the full range of sentence diversity. 

**PLAN.md link:** [Link to PLAN.md](https://github.com/carlinnv/pathreview/blob/fix/151-bias-detector-too-narrow/PLAN.md)

<!-- **Walkthrough video (recommended):** [link to your Loom video, ≤2 min — recommended, not graded] -->

**Blockers or open questions:**
One thing that stood out to me was that in one of the tests, a factual observation was flagged as biased, while a biased assumption was not. Something that I want to consider is how I can ensure that all biased sentences are captured while also keeping a balance and making sure that factual observations do not get flagged as biased. 