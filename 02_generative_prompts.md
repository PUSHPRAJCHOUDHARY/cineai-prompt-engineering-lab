# ✨ Generative Prompts

> **Goal:** Design prompts that instruct an AI to *create* original content — stories, scripts, taglines, dialogue, synopses — in the cinema domain.

---

## What Are Generative Prompts?

Generative prompts ask the AI to produce **new, original content** rather than retrieve or explain existing information. The quality heavily depends on how well constraints, tone, format, and context are specified.

---

## Prompt 1 — Movie Tagline Generator

### ❌ Weak Prompt
```
Write a tagline for a movie.
```

### ✅ Strong Prompt
```
Generate 5 unique movie taglines for the following film concept:

Genre: Psychological Thriller  
Setting: A futuristic city where memories can be bought and sold  
Tone: Dark, mysterious, thought-provoking  
Target audience: Adults aged 25–40  

Requirements:
- Each tagline must be under 12 words
- At least 2 should include a question
- Avoid clichés like "one man's journey" or "nothing is as it seems"
- Number each tagline
```

**Sample Output Generated:**
1. What would you pay to forget everything you love?
2. Your memories. Their market. No refunds.
3. In a city of sold pasts, she remembered everything.
4. Buy. Sell. Forget. Repeat.
5. She paid to forget him. He paid to remember her.

---

## Prompt 2 — Short Film Synopsis Generator

### ❌ Weak Prompt
```
Write a movie synopsis.
```

### ✅ Strong Prompt
```
Write a 100-word synopsis for an original short film with these parameters:

- Genre: Drama with elements of science fiction
- Main character: A 70-year-old woman who discovers she has been living in a simulation
- Emotional core: Grief and acceptance
- Ending type: Open-ended (do not resolve everything)
- Tone: Quiet, introspective, poetic

Format: Single paragraph, present tense, third-person perspective.
Do not use bullet points.
```

---

## Prompt 3 — Dialogue Scene Writer

### ❌ Weak Prompt
```
Write a conversation between two characters.
```

### ✅ Strong Prompt
```
Write a 10-line screenplay dialogue scene between:

CHARACTER A: MEERA, 32, a data scientist who just discovered her company's AI 
             is making life-or-death medical decisions without human review
CHARACTER B: RAJAN, 55, her CEO, pragmatic and profit-driven

Scene context: They are alone in a conference room at 11 PM.
Meera confronts Rajan about the AI system. 

Tone: Tense, professional, with underlying fear
Subtext: Meera is recording the conversation on her phone

Format: Standard screenplay format
  CHARACTER NAME (centered, caps)
  Dialogue (below name, indented)
Include 2 stage directions in parentheses (italics/brackets).
```

---

## Prompt 4 — Movie Review Generator

### ❌ Weak Prompt
```
Write a movie review.
```

### ✅ Strong Prompt
```
Write a 150-word movie review written from the perspective of a regular 
audience member (not a film critic) for a fictional movie called 
"The Quiet Algorithm" — a drama about an AI that learns to grieve.

Requirements:
- Written in first person
- Include one specific scene they loved (you can invent it)
- Include one minor complaint
- End with a recommendation and a rating out of 5 stars
- Avoid technical film jargon — write like a regular person on IMDb
- Tone: Genuine, warm, slightly emotional
```

---

## Prompt 5 — Movie Pitch Document Generator

### ❌ Weak Prompt
```
Pitch a movie idea.
```

### ✅ Strong Prompt
```
Create a one-page movie pitch document for the following concept:

Title: "Signal Lost"
Concept: An astronaut stranded on Mars must communicate with Earth 
         using only emoji because the text codec is corrupted.
Genre: Sci-fi Comedy
Director style inspiration: Wes Anderson meets Stanley Kubrick

Structure the pitch with these exact sections:
1. LOGLINE (1 sentence)
2. THE HOOK (2 sentences — why audiences will care)
3. MAIN CHARACTER (3 bullet points)
4. THREE-ACT STRUCTURE (3 short paragraphs — Setup, Conflict, Resolution)
5. WHY NOW? (1 paragraph — why this story is relevant today)
6. COMPARABLE FILMS (2 movies with a one-line explanation each)

Tone: Professional but creative. This is for a studio executive.
```

---

## 📊 Generative Prompt Scores

| Prompt | Accuracy | Relevance | Clarity | Tone | Completeness | Total |
|---|---|---|---|---|---|---|
| P1 Tagline | 5 | 5 | 5 | 5 | 5 | 25/25 |
| P2 Synopsis | 5 | 5 | 4 | 5 | 4 | 23/25 |
| P3 Dialogue | 4 | 5 | 5 | 5 | 4 | 23/25 |
| P4 Review | 5 | 5 | 5 | 5 | 4 | 24/25 |
| P5 Pitch | 5 | 5 | 5 | 4 | 5 | 24/25 |

**Average: 23.8/25**

---

## 💡 Key Insight from Generative Prompts

> The more **creative freedom** you give without constraints, the more **generic** the output becomes.
> Paradoxically, **more restrictions = more creative and unique output** from an LLM.
> The best generative prompts define the *boundaries*, not the *content*.
