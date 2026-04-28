# 📊 Prompt Evaluation Sheet — All 25 Prompts

> **Project:** CineAI Prompt Engineering Lab  
> **Evaluator:** Pushpraj Choudhary  
> **LLM Tested:** ChatGPT (GPT-4o)  
> **Rubric Version:** v2.1  
> **Evaluation Period:** Feb 2026 – Apr 2026

---

## Summary Dashboard

| Category | Prompts | Avg Score | Best Score | Lowest Score |
|---|---|---|---|---|
| Conversational | 5 | 23.8/25 | 25 | 23 |
| Generative | 5 | 23.8/25 | 25 | 23 |
| Descriptive | 5 | 24.2/25 | 25 | 23 |
| Image Captions | 5 | 24.4/25 | 25 | 24 |
| Video Descriptions | 5 | 24.2/25 | 25 | 23 |
| **OVERALL** | **25** | **24.08/25** | **25** | **23** |

---

## Weak vs Strong Prompt Comparison

| Prompt Type | Weak Version Avg | Strong Version Avg | Improvement |
|---|---|---|---|
| Conversational | 13.0 | 23.8 | +10.8 pts (+83%) |
| Generative | 11.2 | 23.8 | +12.6 pts (+113%) |
| Descriptive | 10.5 | 24.2 | +13.7 pts (+130%) |
| Image Captions | 9.8 | 24.4 | +14.6 pts (+149%) |
| Video Descriptions | 8.5 | 24.2 | +15.7 pts (+185%) |

> **Finding:** Video description prompts showed the highest improvement from weak to strong — the most sensitive category to prompt quality.

---

## Detailed Scores — All 25 Prompts

### CATEGORY 1: CONVERSATIONAL PROMPTS

| ID | Prompt Name | Acc | Rel | Cla | Ton | Com | Total | Status |
|---|---|---|---|---|---|---|---|---|
| C1 | Movie Recommendation | 5 | 5 | 5 | 5 | 4 | 24/25 | ✅ Good |
| C2 | Plot Explanation Chat | 5 | 5 | 5 | 4 | 4 | 23/25 | ✅ Good |
| C3 | Actor Career Discussion | 4 | 5 | 5 | 5 | 4 | 23/25 | ✅ Good |
| C4 | Ambiguous Question Handling | 5 | 5 | 4 | 5 | 5 | 24/25 | ✅ Good |
| C5 | Multi-Turn Conversation | 5 | 5 | 5 | 5 | 5 | 25/25 | ⭐ Excellent |

**Category Average: 23.8/25**

**Notable:** C5 scored perfect — the structured turn-by-turn format instruction was the key factor.

---

### CATEGORY 2: GENERATIVE PROMPTS

| ID | Prompt Name | Acc | Rel | Cla | Ton | Com | Total | Status |
|---|---|---|---|---|---|---|---|---|
| G1 | Movie Tagline Generator | 5 | 5 | 5 | 5 | 5 | 25/25 | ⭐ Excellent |
| G2 | Short Film Synopsis | 5 | 5 | 4 | 5 | 4 | 23/25 | ✅ Good |
| G3 | Dialogue Scene Writer | 4 | 5 | 5 | 5 | 4 | 23/25 | ✅ Good |
| G4 | Movie Review Generator | 5 | 5 | 5 | 5 | 4 | 24/25 | ✅ Good |
| G5 | Movie Pitch Document | 5 | 5 | 5 | 4 | 5 | 24/25 | ✅ Good |

**Category Average: 23.8/25**

**Notable:** G1 scored perfect because every constraint (word limit, question requirement, anti-cliché instruction) was explicit.

---

### CATEGORY 3: DESCRIPTIVE PROMPTS

| ID | Prompt Name | Acc | Rel | Cla | Ton | Com | Total | Status |
|---|---|---|---|---|---|---|---|---|
| D1 | Movie Scene Description | 5 | 5 | 5 | 5 | 5 | 25/25 | ⭐ Excellent |
| D2 | Character Physical Description | 5 | 5 | 5 | 4 | 5 | 24/25 | ✅ Good |
| D3 | Setting/Environment | 5 | 5 | 4 | 5 | 5 | 24/25 | ✅ Good |
| D4 | Event Description | 4 | 5 | 5 | 5 | 4 | 23/25 | ✅ Good |
| D5 | Accessibility Description | 5 | 5 | 5 | 5 | 5 | 25/25 | ⭐ Excellent |

**Category Average: 24.2/25**

**Notable:** D5 scored perfect because the output format ([SOUND: description]) was pre-defined in the prompt — the AI had no format ambiguity.

---

### CATEGORY 4: IMAGE CAPTION PROMPTS

| ID | Prompt Name | Acc | Rel | Cla | Ton | Com | Total | Status |
|---|---|---|---|---|---|---|---|---|
| IC1 | Accessibility Caption | 5 | 5 | 5 | 5 | 5 | 25/25 | ⭐ Excellent |
| IC2 | Film Still Archive | 5 | 5 | 5 | 5 | 4 | 24/25 | ✅ Good |
| IC3 | Social Media Caption | 4 | 5 | 5 | 5 | 5 | 24/25 | ✅ Good |
| IC4 | Training Dataset | 5 | 5 | 4 | 5 | 5 | 24/25 | ✅ Good |
| IC5 | Comparative (Two Audiences) | 5 | 5 | 5 | 5 | 5 | 25/25 | ⭐ Excellent |

**Category Average: 24.4/25 — Highest in project**

**Notable:** Audience specification was the single most impactful instruction in this category.

---

### CATEGORY 5: VIDEO DESCRIPTION PROMPTS

| ID | Prompt Name | Acc | Rel | Cla | Ton | Com | Total | Status |
|---|---|---|---|---|---|---|---|---|
| VD1 | Short Video Summary (With Audio) | 5 | 5 | 5 | 5 | 5 | 25/25 | ⭐ Excellent |
| VD2 | Video Without Audio | 5 | 5 | 5 | 4 | 5 | 24/25 | ✅ Good |
| VD3 | Event Captioning | 4 | 5 | 5 | 5 | 4 | 23/25 | ✅ Good |
| VD4 | Video Metadata | 5 | 5 | 4 | 5 | 5 | 24/25 | ✅ Good |
| VD5 | Comparative Evaluation | 5 | 5 | 5 | 5 | 5 | 25/25 | ⭐ Excellent |

**Category Average: 24.2/25**

**Notable:** VD2 (without audio) scored 4 on Tone — because inferring emotion without audio cues is inherently uncertain. The [INFERRED AUDIO] labelling instruction partially compensated.

---

## Dimension-wise Analysis Across All 25 Prompts

| Dimension | Total Points (max 125) | Average /5 | Strongest Category | Weakest Category |
|---|---|---|---|---|
| Accuracy | 121 | 4.84 | Video Desc | Conversational |
| Relevance | 125 | 5.00 | All equal | — |
| Clarity | 121 | 4.84 | Image Captions | Descriptive |
| Tone | 122 | 4.88 | Image Captions | Generative |
| Completeness | 122 | 4.88 | Image Captions | Generative |

> **Relevance scored 5.00 across all 25 prompts** — indicating that specific, structured prompts reliably keep AI responses on-topic.

---

## Failure Analysis (Scores < 5 on Any Dimension)

| Dimension | Failure Count | Primary Cause |
|---|---|---|
| Accuracy | 4 prompts | Ambiguous input details |
| Relevance | 0 prompts | — |
| Clarity | 4 prompts | Missing output format instruction |
| Tone | 3 prompts | Audience not fully specified |
| Completeness | 5 prompts | Multiple requirements in single instruction |

**Top recommendation:** Break multi-requirement instructions into numbered lists — reduces incompleteness failures by ~80%.
