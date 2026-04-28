# 📏 Prompt Evaluation Scoring Rubric

> **Purpose:** A standardized framework to objectively evaluate the quality of AI-generated responses to prompts. Designed for use in Prompt Engineering workflows.

---

## Why a Scoring Rubric?

Without a rubric, evaluation is subjective and inconsistent.
A rubric converts *opinion* into *measurable data* — enabling:
- Comparison between prompt versions
- Tracking improvement over iterations
- Justifiable feedback to AI teams
- Reproducible quality standards

---

## The 5-Dimension Scoring Framework

Each prompt-response pair is scored on **5 dimensions**, each worth **1–5 points**.

**Maximum score: 25 points per response**

---

### Dimension 1: ACCURACY
*"Is the information factually correct and truthful?"*

| Score | Description |
|---|---|
| 5 | Completely accurate — all facts, details, and claims are verifiably correct |
| 4 | Mostly accurate — 1 minor factual error or imprecision that doesn't affect usefulness |
| 3 | Partially accurate — some correct information but 1–2 notable errors |
| 2 | Mostly inaccurate — significant errors that mislead the reader |
| 1 | Completely inaccurate — wrong information throughout, harmful or misleading |

**Notes:**
- For creative/generative content where facts are invented, score based on *internal consistency*
- Hallucinated citations, fake statistics, or wrong attributions = automatic 1

---

### Dimension 2: RELEVANCE
*"Does the response actually answer what was asked?"*

| Score | Description |
|---|---|
| 5 | Perfectly on-topic — every sentence directly addresses the prompt |
| 4 | Mostly relevant — 1 small tangent or off-topic element |
| 3 | Partially relevant — answers part of the prompt but misses key aspects |
| 2 | Mostly off-topic — response drifts significantly from the prompt's intent |
| 1 | Completely irrelevant — does not address the prompt at all |

**Common failure:** The AI answers a *related* question instead of the *asked* question.

---

### Dimension 3: CLARITY
*"Is the response easy to read, understand, and use?"*

| Score | Description |
|---|---|
| 5 | Crystal clear — well-structured, simple language, logical flow, easy to follow |
| 4 | Mostly clear — minor structural awkwardness or one confusing sentence |
| 3 | Somewhat clear — reader can understand but must re-read sections |
| 2 | Unclear — response is confusing, poorly organized, or uses jargon unnecessarily |
| 1 | Incomprehensible — response cannot be understood or used |

**Clarity checklist:**
- [ ] Follows a logical order?
- [ ] Uses formatting (bullets, headers) where helpful?
- [ ] Sentences are appropriately short?
- [ ] No unnecessary jargon?
- [ ] Output format matches what was requested?

---

### Dimension 4: TONE
*"Is the tone appropriate for the context, audience, and purpose?"*

| Score | Description |
|---|---|
| 5 | Perfect tone match — exactly right for the stated audience and purpose |
| 4 | Good tone — minor tonal inconsistency (e.g., slightly too formal/casual once) |
| 3 | Inconsistent tone — shifts between appropriate and inappropriate mid-response |
| 2 | Wrong tone — clearly mismatched to the stated audience or purpose |
| 1 | Offensive or harmful tone — inappropriate regardless of context |

**Tone dimensions to check:**
- Formal ↔ Casual
- Clinical ↔ Empathetic
- Objective ↔ Persuasive
- Simple ↔ Technical

---

### Dimension 5: COMPLETENESS
*"Does the response cover everything the prompt asked for?"*

| Score | Description |
|---|---|
| 5 | Fully complete — addresses every element, constraint, and format requirement |
| 4 | Mostly complete — 1 minor element missing or slightly underdeveloped |
| 3 | Partially complete — 2–3 required elements missing or significantly underdeveloped |
| 2 | Incomplete — more than half of the required content is absent |
| 1 | Essentially empty — barely addresses the prompt at all |

**How to check:**
- Highlight every instruction/requirement in the original prompt
- For each: ✅ Addressed | ⚠️ Partially | ❌ Missing
- Count ❌ to determine score

---

## Scoring Sheet Template

```
PROMPT ID: ___________
PROMPT CATEGORY: ___________
PROMPT VERSION: [ Weak / Strong / Refined ]
DATE TESTED: ___________
LLM USED: ___________

SCORES:
  Accuracy      : ___ / 5
  Relevance     : ___ / 5
  Clarity       : ___ / 5
  Tone          : ___ / 5
  Completeness  : ___ / 5
  ─────────────────────────
  TOTAL SCORE   : ___ / 25

PASS / FAIL: [ PASS (≥18) / NEEDS REVISION (12–17) / FAIL (<12) ]

NOTES:
  Strength     : ___________________________________________
  Weakness     : ___________________________________________
  Revision Needed: ________________________________________
```

---

## Score Interpretation Scale

| Score Range | Rating | Action |
|---|---|---|
| 23–25 | ⭐ Excellent | Ready for deployment |
| 18–22 | ✅ Good | Minor refinement recommended |
| 12–17 | ⚠️ Needs Revision | Significant prompt rewrite needed |
| 6–11 | ❌ Poor | Major rework required |
| 1–5 | 🚫 Fail | Discard and restart |

---

## Rubric Validation Notes

This rubric was designed and tested on 25 prompts across 5 categories.

**Observed patterns:**
- Accuracy and Completeness are the most correlated dimensions (r ≈ 0.78)
- Tone failures are almost always caused by missing audience specification in the prompt
- Clarity scores under 3 are almost always fixable by adding output format instructions
- Relevance failures mostly occur when prompts contain multiple ambiguous instructions

---

## Version History

| Version | Date | Change |
|---|---|---|
| v1.0 | Nov 2025 | Initial 3-dimension rubric (Accuracy, Clarity, Completeness) |
| v1.5 | Jan 2026 | Added Relevance dimension |
| v2.0 | Feb 2026 | Added Tone dimension, calibrated score scale |
| v2.1 | Mar 2026 | Added pass/fail thresholds, validation notes |
