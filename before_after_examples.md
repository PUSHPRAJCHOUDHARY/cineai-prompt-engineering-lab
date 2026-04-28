# 🔄 Before & After — Prompt Refinement Case Studies

> **Purpose:** Demonstrate iterative prompt improvement using real examples.  
> Each case shows: Original Prompt → Problem Analysis → Refined Prompt → Score Improvement.

---

## What Is Iterative Refinement?

Prompt engineering is not a one-shot process. Like editing a document, the first version is a draft. Refinement means:
1. Testing the prompt on an LLM
2. Identifying what went wrong in the output
3. Modifying the prompt to fix those failures
4. Re-testing and re-scoring

This file documents **10 refinement cycles** from this project.

---

## Case Study 1 — Movie Recommendation Prompt

### Version 1 (Original)
```
Suggest some movies.
```
**Score: 10/25** | Problem: No context → generic Hollywood blockbuster list

### Version 2 (First Refinement)
```
Suggest 5 thriller movies.
```
**Score: 15/25** | Problem: Still no user context, no format, no tone

### Version 3 (Final)
```
You are a friendly movie recommendation assistant. 
The user enjoys psychological thrillers with plot twists, 
similar to "Gone Girl" and "Shutter Island".
Recommend 3 movies. For each: title, year, one-line reason, mood rating (Light/Medium/Intense).
Keep tone conversational and enthusiastic.
```
**Score: 24/25** | Fixed by: Role + preference context + structured format + tone instruction

**Score gain: +14 points (+140%) across 3 versions**

---

## Case Study 2 — Video Summary Without Audio

### Version 1 (Original)
```
Describe a video without sound.
```
**Score: 8/25** | Problem: AI just wrote a visual description — missed the challenge entirely

### Version 2 (First Refinement)
```
Describe this video. The audio is not available. 
Infer what sounds might be present.
```
**Score: 14/25** | Better but: no timestamps, no format, ambiguous "infer" instruction

### Version 3 (Final)
```
Write an audio description for a video clip where audio is NOT available.
Use visual cues only.
Time-stamp each action (00:00, 00:10, etc.)
Label inferred sounds as: [INFERRED AUDIO: description]
Flag ambiguous moments as [UNCLEAR — NEEDS AUDIO CONFIRMATION]
Keep each description under 15 words per timestamp.
```
**Score: 24/25** | Fixed by: Explicit labelling format, timestamps, uncertainty flagging

**Score gain: +16 points (+200%) across 3 versions**

---

## Case Study 3 — Character Description

### Version 1 (Original)
```
Describe a movie character.
```
**Output problem:** AI invented everything including personality, backstory, full life history — unusable for casting.

**Score: 9/25**

### Version 2 (Refined)
```
Describe only the physical appearance of a female scientist character 
for a casting brief. Age: early 40s. Do not include personality or backstory.
Format as a numbered list.
```
**Score: 22/25** | Minor issue: AI still included one personality note

### Version 3 (Final — added explicit exclusion)
```
Describe ONLY physical appearance (build, face, eyes, hair, posture, clothing).
Do NOT include: personality traits, backstory, intelligence, job performance.
If you include any non-physical trait, your response fails the requirement.
Format: numbered list. Length: 80–100 words.
```
**Score: 24/25** | Key fix: Explicit exclusion list + consequence framing

**Lesson:** Telling AI what NOT to include is as important as what to include.

---

## Case Study 4 — Social Media Caption

### Version 1 (Original)
```
Write a social media caption for a movie.
```
**Problem:** AI wrote one generic Instagram caption. Missed the platform differences entirely.

**Score: 11/25**

### Version 2 (Refined — added platform)
```
Write Instagram, Twitter, and LinkedIn captions for this movie image.
[Image described]
```
**Score: 18/25** | Better — got 3 captions, but tone was same across all 3

### Version 3 (Final — explicit tone per platform)
```
INSTAGRAM: Emotional, poetic, 2–3 sentences, 3–5 hashtags, max 2 emoji
TWITTER/X: Under 240 chars, punchy, 1 question or bold statement, 2 hashtags
LINKEDIN: Professional, no hashtags, no emoji, team achievement angle, 3 sentences
```
**Score: 24/25** | Fixed by: Platform-specific tone, format, constraint per channel

**Lesson:** When writing for multiple platforms, specify constraints *per platform*, not globally.

---

## Case Study 5 — Dialogue Scene

### Version 1 (Original)
```
Write a conversation between two people.
```
**Output:** Casual small talk. No tension. No context. Unusable.

**Score: 8/25**

### Version 2 (Refined)
```
Write a 10-line argument between a CEO and an employee about an AI ethics issue.
Format as a screenplay.
```
**Score: 17/25** | Improvement, but characters were flat and generic

### Version 3 (Final)
```
Write a 10-line screenplay dialogue.
CHARACTER A: MEERA, 32, data scientist discovering unethical AI use
CHARACTER B: RAJAN, 55, CEO, pragmatic and profit-driven
Setting: Conference room, 11 PM, late night — high stakes
Subtext: Meera is secretly recording the conversation
Tone: Tense, professional, fear underneath
Format: CHARACTER NAME (caps, centered) / Dialogue / 2 stage directions in brackets
```
**Score: 23/25** | Fixed by: Character depth, subtext instruction, specific format

**Lesson:** Characters need **one defining tension** beyond their title. Generic roles = generic dialogue.

---

## Case Study 6 — Accessibility Scene Description

### Version 1 (Original)
```
Describe this scene for blind people.
```
**Problem:** AI wrote a visual-only description — ignored that blind users also need audio described.

**Score: 12/25**

### Version 2 (Refined)
```
Write an accessibility description of this scene for visually impaired users.
Include sounds and atmosphere, not just visuals.
```
**Score: 19/25** | Better, but no sensory priority order

### Version 3 (Final)
```
Write an accessibility description. Cover in this order:
1. What is happening (action)
2. Visual details (colors, expressions, lighting)
3. Sounds and ambient audio
4. Emotional atmosphere conveyed by the scene

Use short sentences (under 15 words each).
Avoid figurative language — be literal and clear.
Length: 100–130 words.
```
**Score: 25/25** | Fixed by: Defined sensory order, sentence length limit, literal instruction

---

## Case Study 7 — AI Response Evaluation Prompt

### Version 1 (Original)
```
Is this a good AI response? [response pasted]
```
**Output:** "Yes, it seems good." — Completely useless.

**Score: 5/25**

### Version 2 (Refined)
```
Evaluate this AI response on accuracy, clarity, and helpfulness.
Score each out of 5.
```
**Score: 16/25** | Scores given but no explanation, no actionable feedback

### Version 3 (Final)
```
You are a senior prompt engineer evaluating an AI response.

Score the following response on 5 dimensions (1–5 each):
1. Accuracy — are facts correct?
2. Relevance — does it answer what was asked?
3. Clarity — is it easy to understand?
4. Tone — appropriate for the audience?
5. Completeness — does it cover everything asked?

For each dimension:
- Give a score
- Write 1 sentence explaining why
- Suggest 1 specific improvement

End with TOTAL SCORE /25 and one overall recommendation.
```
**Score: 25/25** | Fixed by: Structured per-dimension format with explanation + improvement requirement

---

## Case Study 8 — Film Archive Caption

### Version 1 (Original)
```
Write a caption for a movie photo.
```
**Output:** "Two actors in a dramatic scene." — Useless for archiving.

**Score: 7/25**

### Version 2 (Refined)
```
Write a formal caption for a film archive. Include film title, character, and shot type.
```
**Score: 16/25** | Structure missing, inconsistent across entries

### Version 3 (Final)
```
Write a 3-line archive caption:
Line 1: [Film Title, Year] — Scene description (objective, factual)
Line 2: Subjects: [character name, not actor name]
Line 3: Technical: [shot type, lighting, setting]
Total: under 60 words. No emotional language. No interpretation.
```
**Score: 24/25** | Fixed by: Exact format template with field labels

**Lesson:** For structured data outputs, provide the *exact template* — don't describe the template, show it.

---

## Case Study 9 — Documentary Narration

### Version 1
```
Write narration for a documentary.
```
**Output:** Generic, excited tone — sounded like an advertisement.

**Score: 11/25**

### Version 2 (Refined)
```
Write documentary narration in a calm, observational style.
Describe an awards ceremony moment — first time winner.
```
**Score: 18/25** | Tone better, but AI still interpreted/editorialized

### Version 3 (Final)
```
Write documentary narration in the style of a BBC nature documentary narrator.
Tone: calm, observational, non-emotional.
Describe ONLY what is seen and heard — no character thoughts, no interpretation.
Present tense. 
Length: 120–150 words.
The subject: First-time filmmaker winning an award at an international film festival.
```
**Score: 23/25** | Fixed by: Specific reference style + no-interpretation constraint + tense

---

## Case Study 10 — Multi-Platform Content Prompt

### Version 1
```
Write content about a new movie for different platforms.
```
**Output:** Four nearly identical paragraphs with slightly different lengths.

**Score: 9/25**

### Version 2 (Refined)
```
Write unique content for Instagram, YouTube description, and a press release for "Red Horizon."
```
**Score: 16/25** | Different but tone was inconsistent and format was same

### Version 3 (Final)
```
For the film "Red Horizon," create 3 pieces of content:

1. INSTAGRAM POST
   - Hook in first line (stops scroll)
   - Emotional language
   - 3 hashtags, 2 emoji max
   - Under 150 characters

2. YOUTUBE VIDEO DESCRIPTION  
   - First 2 lines visible without expanding (must hook)
   - Include: cast mention, release date, genre
   - SEO keywords: survival, mars, sci-fi 2026, space drama
   - 100–120 words total

3. PRESS RELEASE OPENING PARAGRAPH
   - Formal journalism style (inverted pyramid)
   - Who, What, When, Where, Why in first 2 sentences
   - No emoji, no hashtags
   - 80 words max
```
**Score: 25/25** | Fixed by: Platform-native format rules, content requirements per platform, character limits

---

## 📊 Refinement Summary

| Case | V1 Score | Final Score | Gain | Key Fix |
|---|---|---|---|---|
| 1 — Movie Rec | 10 | 24 | +14 | Role + format + tone |
| 2 — Video No Audio | 8 | 24 | +16 | Timestamps + label format |
| 3 — Character Desc | 9 | 24 | +15 | Explicit exclusions |
| 4 — Social Caption | 11 | 24 | +13 | Per-platform constraints |
| 5 — Dialogue Scene | 8 | 23 | +15 | Character subtext + format |
| 6 — Accessibility | 12 | 25 | +13 | Sensory order + sentence limit |
| 7 — AI Evaluation | 5 | 25 | +20 | Structured scoring template |
| 8 — Archive Caption | 7 | 24 | +17 | Exact template provided |
| 9 — Narration | 11 | 23 | +12 | Style reference + no-interp |
| 10 — Multi-Platform | 9 | 25 | +16 | Per-platform format rules |

**Average V1 Score: 9.0/25**  
**Average Final Score: 24.1/25**  
**Average Improvement: +15.1 points per prompt (+168%)**
