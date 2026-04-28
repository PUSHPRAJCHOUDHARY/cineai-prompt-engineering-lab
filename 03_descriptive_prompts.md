# 📝 Descriptive Prompts

> **Goal:** Design prompts that generate rich, detailed, accurate descriptions of scenes, characters, environments, and events — a core skill for AI content systems.

---

## What Are Descriptive Prompts?

Descriptive prompts ask the AI to **paint a picture with words** — for accessibility tools, content cataloguing, AI training data, or user-facing content. Precision, sensory detail, and structured format are critical.

---

## Prompt 1 — Movie Scene Description

### ❌ Weak Prompt
```
Describe a movie scene.
```

### ✅ Strong Prompt
```
Write a detailed description of the following fictional movie scene for use in 
an AI training dataset. The description will be read by people with visual impairments.

Scene details:
- Location: A crowded train station in 1940s Paris, early morning
- Characters: A young woman in a red coat carrying a suitcase, an older man in a grey uniform
- Action: She is trying to board a train. He stops her and checks her papers.
- Mood: Tense, fearful

Instructions:
- Describe in present tense
- Include visual details (colors, lighting, expressions, posture)
- Include ambient sounds and atmosphere
- Do NOT include character thoughts or backstory
- Length: 100–130 words
- Use short, clear sentences for accessibility
```

---

## Prompt 2 — Character Physical Description

### ❌ Weak Prompt
```
Describe a movie character.
```

### ✅ Strong Prompt
```
Generate a detailed physical description of a fictional movie character 
for use in a casting brief. This description will help casting directors 
understand who they are looking for.

Character profile:
- Name: DR. ARIA SETH
- Role: Lead scientist who uncovers a government cover-up
- Age: Early 40s
- Background: Originally from a small coastal town, now works in a high-tech lab
- Personality hint: Brilliant but emotionally guarded

Describe ONLY physical appearance:
- Build and height
- Face (specific features)
- Eyes and hair
- How they carry themselves (posture, gait)
- Signature clothing/accessory detail

Do NOT mention personality traits or backstory.
Format as a numbered list.
Length: 80–100 words.
```

---

## Prompt 3 — Setting/Environment Description

### ❌ Weak Prompt
```
Describe a location.
```

### ✅ Strong Prompt
```
Write an immersive description of the following film location for a 
production design brief. This will be used to guide set construction.

Location: The villain's underground laboratory  
Film genre: Sci-fi thriller  
Era: Near future (2045)  
Visual style reference: Cold, clinical, with hidden chaos underneath  
Lighting: Predominantly blue-white with patches of red emergency lights  

Cover these elements in order:
1. Overall size and layout (2 sentences)
2. Walls, floors, ceiling (2 sentences)
3. Equipment and furniture (3 sentences)
4. Lighting and atmosphere (2 sentences)
5. One unexpected/distinctive detail that makes it memorable (1 sentence)

Tone: Professional production writing style.
```

---

## Prompt 4 — Event Description (Non-Fiction Style)

### ❌ Weak Prompt
```
Describe an award ceremony.
```

### ✅ Strong Prompt
```
Write a descriptive account of the following event for a documentary narration script.
The narrator has a calm, observational tone similar to a BBC documentary.

Event: The moment a first-time filmmaker from a small Indian town wins 
       the Best Director award at a major international film festival.

Describe:
- The physical environment of the auditorium in that moment
- The audience's reaction (general, not specific people)
- The winner's journey from their seat to the stage (movement, expression)
- The podium moment (physical setting, the trophy, the microphone)

Constraints:
- Present tense
- No dialogue or speech content
- No emotional interpretation — describe only what is SEEN and HEARD
- 120–150 words
```

---

## Prompt 5 — Accessibility Description (for Deaf/HoH Audience)

### ❌ Weak Prompt
```
Describe what's happening in a video.
```

### ✅ Strong Prompt
```
Write an audio description for a 30-second scene from a movie. 
This description will be used as closed captions for Deaf and Hard-of-Hearing audiences 
and must convey ALL audio information that hearing viewers receive.

Scene: Two characters are arguing in a kitchen. 
  - Character A slams a glass on the counter
  - A phone rings in the background — neither answers
  - Character B starts to cry quietly, turns away
  - Door slams. Silence.
  - A clock ticking becomes audible

Instructions:
- Describe each sound event with its emotional implication in brackets
- Format: [SOUND: description] on its own line before the visual action it accompanies
- Include ambient/background sounds
- Keep language simple and immediate
- Each description: under 10 words
```

**Sample Output:**
```
[SOUND: Glass slams on counter — sharp, angry]
[SOUND: Phone ringing — distant, unanswered]
[SOUND: Quiet crying — stifled, suppressed]
[SOUND: Door slams — final, definitive]
[SOUND: Clock ticking — steady, isolating silence]
```

---

## 📊 Descriptive Prompt Scores

| Prompt | Accuracy | Relevance | Clarity | Tone | Completeness | Total |
|---|---|---|---|---|---|---|
| P1 Scene | 5 | 5 | 5 | 5 | 5 | 25/25 |
| P2 Character | 5 | 5 | 5 | 4 | 5 | 24/25 |
| P3 Setting | 5 | 5 | 4 | 5 | 5 | 24/25 |
| P4 Event | 4 | 5 | 5 | 5 | 4 | 23/25 |
| P5 Accessibility | 5 | 5 | 5 | 5 | 5 | 25/25 |

**Average: 24.2/25 — Highest category average in this project**

---

## 💡 Key Insight

> Descriptive prompts benefit most from **sensory layering instructions** — telling the AI 
> *which senses* to address (sight, sound, texture) dramatically improves output quality.
> Without this, LLMs default to visual-only descriptions and miss 40–60% of scene richness.
