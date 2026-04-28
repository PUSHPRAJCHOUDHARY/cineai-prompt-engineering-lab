# 🖼️ Image Caption Prompts

> **Goal:** Design prompts that generate accurate, useful, and context-appropriate captions for images — a key task in AI systems for accessibility, content tagging, and search indexing.

---

## What Are Image Caption Prompts?

Image captioning prompts instruct an AI to describe visual content in a concise, informative way. The caption style changes based on purpose:
- **Accessibility captions** → For visually impaired users (detailed, functional)
- **Social media captions** → Engaging, short, with personality
- **Metadata/indexing captions** → Factual, keyword-rich, no emotion
- **Film archive captions** → Formal, scene-specific, time-stamped

---

## Prompt 1 — Accessibility Caption (Alt Text)

### ❌ Weak Prompt
```
Write a caption for this image.
[Image: Two people talking in a cafe]
```

### ✅ Strong Prompt
```
Write an alt-text accessibility caption for the following image.
This caption will be read by screen readers to visually impaired users.

Image content:
- Two people seated across from each other at a small wooden café table
- One person: young woman, mid-20s, leaning forward, gesturing with hands
- Other person: older man, 50s, arms crossed, looking skeptical
- Setting: Warm, busy café — blurred patrons in background, coffee cups on table
- Lighting: Natural window light from the left, creating soft shadows

Requirements:
- Start with the most important element (the people and their interaction)
- Describe left to right, foreground to background
- Include emotional tone conveyed by body language
- Under 50 words
- Do NOT say "image of" or "picture of" — start directly with content
```

**Sample Output:**
> Two people sit at a small wooden café table in conversation. A young woman leans forward, gesturing expressively, while an older man sits with arms crossed, appearing skeptical. Warm natural light streams from the left. A busy café is visible in the background.

---

## Prompt 2 — Film Still Caption (Archive Use)

### ❌ Weak Prompt
```
Describe this movie image.
```

### ✅ Strong Prompt
```
Write a formal archive caption for a film still photograph.
This caption will be stored in a digital film archive database.

Image details:
- Film: Fictional title "The Glass Meridian" (2024)
- Scene: Exterior shot, night, rooftop of a skyscraper
- Subject: Lead actor (fictional: Marcus Venn) standing at the edge, looking down at the city
- Costume: Long dark coat, no hat, wind-blown hair
- Technical: Wide shot, low angle, city lights bokeh in background

Format your caption as:
Line 1: [Film Title, Year] — Scene description (objective, factual)
Line 2: Subjects identified (character name, not actor name)
Line 3: Technical details (shot type, lighting, setting)

Total: Under 60 words. No emotional language.
```

---

## Prompt 3 — Social Media Caption

### ❌ Weak Prompt
```
Write a social media post for a movie image.
```

### ✅ Strong Prompt
```
Write 3 different social media captions for the same movie promotional image.

Image: A dramatic wide shot of a lone astronaut standing on a Martian cliff, 
       looking at a double sunset, small Earth visible in the sky.
Film: "Red Horizon" — a survival sci-fi drama

Write one caption for each platform:

INSTAGRAM: 
- Emotional, poetic, 2–3 sentences max
- 3–5 relevant hashtags at the end
- Emoji: 1–2 maximum

TWITTER/X:
- Punchy, under 240 characters including hashtags
- One rhetorical question or bold statement
- 2 hashtags max

LINKEDIN (for the film production company):
- Professional tone announcing the film
- Mention team achievement angle
- No hashtags, no emoji
- 3 sentences max
```

---

## Prompt 4 — Caption for AI Training Dataset

### ❌ Weak Prompt
```
Label this image.
```

### ✅ Strong Prompt
```
Generate a structured image caption for an AI vision model training dataset.
The caption must be machine-readable and follow strict formatting rules.

Image content:
- Indoor setting: hospital waiting room
- People: 3 adults seated, 1 child standing, 1 nurse walking in background
- Objects: Plastic chairs (blue), a TV mounted on wall (news channel on), 
           a reception desk, potted plant in corner
- Lighting: Fluorescent overhead lighting, slightly harsh
- Emotional atmosphere: Tense, waiting

Output format — fill in ALL fields:
SCENE_TYPE: [indoor/outdoor]
LOCATION: [specific place]
PEOPLE_COUNT: [number]
PEOPLE_DESCRIPTION: [age groups, actions, positions]
KEY_OBJECTS: [comma-separated list]
LIGHTING: [type and quality]
MOOD: [single adjective]
DETAILED_CAPTION: [1–2 sentence natural language description]
```

---

## Prompt 5 — Comparative Caption (Same Image, Two Audiences)

### ✅ Strong Prompt
```
Write two different captions for the same image, targeted at two different audiences.

Image: A behind-the-scenes photo from a film set showing a female director 
       standing next to a large cinema camera, pointing at a monitor, 
       surrounded by crew members watching attentively.

CAPTION A — Target: Children (age 8–12) for an educational website about careers
- Simple vocabulary
- Inspiring tone
- Under 30 words
- Explain what a director does in 1 sentence

CAPTION B — Target: Film industry professionals for a trade magazine
- Technical vocabulary is appropriate
- Focus on the professional setting and role
- Under 40 words
- Do not explain what a director does (assumed knowledge)

Label each caption clearly as CAPTION A and CAPTION B.
```

---

## 📊 Image Caption Prompt Scores

| Prompt | Accuracy | Relevance | Clarity | Tone | Completeness | Total |
|---|---|---|---|---|---|---|
| P1 Accessibility | 5 | 5 | 5 | 5 | 5 | 25/25 |
| P2 Archive | 5 | 5 | 5 | 5 | 4 | 24/25 |
| P3 Social Media | 4 | 5 | 5 | 5 | 5 | 24/25 |
| P4 Training Data | 5 | 5 | 4 | 5 | 5 | 24/25 |
| P5 Comparative | 5 | 5 | 5 | 5 | 5 | 25/25 |

**Average: 24.4/25**

---

## 💡 Key Insight

> The **purpose of the caption** must be defined in the prompt — the same image 
> needs completely different language for a child, a screen reader, and a database index.
> Audience-first thinking is the most important principle in caption prompt design.
