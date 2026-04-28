# 🎥 Video Description Prompts

> **Goal:** Design prompts that generate accurate, structured descriptions of video content — both WITH and WITHOUT audio — for accessibility, content indexing, and AI training.

---

## What Are Video Description Prompts?

Video descriptions translate dynamic visual+audio content into text. They are used for:
- **Audio descriptions** for blind/visually impaired viewers
- **Closed captions** for deaf/HoH viewers  
- **Content metadata** for search and recommendation systems
- **AI training datasets** for video understanding models

Key challenge: Video has a **time dimension** that static images don't. Prompts must account for sequence, duration, transitions, and audio-visual sync.

---

## Prompt 1 — Short Video Summary (With Audio)

### ❌ Weak Prompt
```
Summarize this video.
```

### ✅ Strong Prompt
```
Write a structured summary for a 90-second movie trailer.
This summary will appear as a text description on a streaming platform.

Trailer content:
- First 20 seconds: Peaceful village scene, children playing, upbeat folk music
- 0:20–0:45: Sudden dark tone shift — storm clouds, villagers running, dramatic orchestral sting
- 0:45–1:10: Rapid montage — hero running, explosions, close-up of determined faces, 
              intense percussion
- 1:10–1:30: Single quiet shot — hero and child holding hands, soft piano note
- 1:30–1:35: Film title appears with deep bass sound effect
- 1:35–1:40: Release date text, silence

Write:
1. OVERVIEW (2 sentences — genre, tone, core conflict)
2. SCENE BREAKDOWN (4 bullet points — one per time segment)
3. AUDIO SUMMARY (2 sentences — describe how music/sound serves the narrative)
4. TAGLINE SUGGESTION (1 sentence — based on what you've described)

Keep total under 200 words.
```

---

## Prompt 2 — Video Description WITHOUT Audio (Visual Only)

### ✅ Strong Prompt
```
Write an audio description for a video clip where audio is NOT available.
The description must compensate for missing audio using only visual cues.

Video clip (visual content only — assume you cannot hear anything):
- Duration: 45 seconds
- Setting: City street, daytime, heavy rain visible
- Person A: Man in a suit, running under an umbrella, looking at his phone frequently
- Person B: Woman sitting on steps, no umbrella, getting wet, watching him
- Action sequence: He drops his phone. She picks it up. Their eyes meet. He reaches for 
                   the phone. She holds it back for a moment, then gives it to him.
                   He looks at her properly for the first time. She smiles slightly.
                   He starts to say something. She shakes her head. He nods and walks away.
                   She watches him go.

Instructions:
- Infer emotional content from VISUAL CUES ONLY (facial expression, body language, pace)
- Note what sounds would LIKELY be present (label as: [INFERRED AUDIO])
- Time-stamp each action (00:00, 00:10, etc.)
- Keep descriptions under 15 words per timestamp
- Flag any ambiguous moments as [UNCLEAR — NEEDS AUDIO CONFIRMATION]
```

---

## Prompt 3 — Event Captioning (Live/Sports Style)

### ✅ Strong Prompt
```
Write live-event style video captions for the following sequence from a 
fictional movie awards ceremony. These captions will appear as real-time 
text for live streaming viewers who have muted their audio.

Sequence (30 seconds):
- Host walks to microphone, adjusts it, shuffles papers
- Opens envelope, pauses dramatically, looks up at audience
- Audience falls silent
- Host reads the winner's name
- Winner (a young woman, first time nominee) gasps, hands over mouth
- Her co-stars seated nearby hug her, some are crying
- She stands, smooths her dress, walks toward stage
- Trips slightly on the stairs — catches herself — audience laughs warmly
- Reaches podium, grips both sides, takes a breath

Caption requirements:
- Each caption: max 42 characters (broadcast standard)
- Use ALL CAPS for spoken content: [WINNER ANNOUNCED]
- Use Title Case for visual actions: Host Opens Envelope
- Include [AUDIENCE REACTION] labels
- Time-stamp every 5 seconds
- Total: 6–8 caption blocks
```

---

## Prompt 4 — Video Content Metadata for Search Indexing

### ✅ Strong Prompt
```
Generate structured metadata tags for the following video content.
This metadata will be used by a streaming platform's search and 
recommendation algorithm.

Video: A 12-minute documentary segment about a female stunt performer 
       working in the Hindi film industry. 
       
Content includes:
- Interview with the performer (talking about training and challenges)
- Footage of her performing motorcycle stunts on a film set
- Brief clips of the movies she has worked on
- Interview with a male director praising her work
- Statistics shown on screen: "Only 8% of Bollywood stunt performers are women"

Generate:
TITLE_TAGS: [5 searchable title keywords]
TOPIC_TAGS: [8 content topic tags]
MOOD_TAGS: [3 emotional/tonal tags]
DEMOGRAPHIC_TAGS: [likely audience segments, 3 max]
CONTENT_WARNINGS: [any sensitive content to flag]
CHAPTER_TIMESTAMPS: [suggested chapter breaks with labels]
SEO_DESCRIPTION: [2 sentence description optimized for search, under 160 characters]
ACCESSIBILITY_NEEDED: [list what accessibility features this video needs]
```

---

## Prompt 5 — Video Comparison Prompt (Two Versions)

### ✅ Strong Prompt
```
You are evaluating two different AI-generated video descriptions of the same clip.
Score each description and explain which is better and why.

ORIGINAL VIDEO CLIP:
A 20-second scene: A father watches his daughter's school play from the back of 
the auditorium. He arrived late. She spots him, mid-performance, and her face 
transforms — she smiles without breaking character. He nods once. She continues.
The audience doesn't notice this exchange.

AI DESCRIPTION VERSION A:
"A man stands at the back of a school auditorium watching a children's play. 
A girl on stage notices him and smiles. He nods back at her."

AI DESCRIPTION VERSION B:
"A father who arrived late to his daughter's school play stands quietly at the 
rear of the auditorium. His daughter, mid-performance, catches sight of him. 
Her expression shifts — a brief, contained smile crosses her face without 
breaking her stage character. He responds with a single nod. The silent exchange 
goes unnoticed by the audience. The moment lasts under three seconds."

Score EACH version on:
- Accuracy (does it match the video content?) /5
- Completeness (does it capture all key events?) /5  
- Emotional Accuracy (does it capture the right feeling?) /5
- Accessibility Value (useful for visually impaired viewer?) /5
- Conciseness (appropriate length, no unnecessary words?) /5

Then: Write your own IMPROVED version that addresses both versions' weaknesses.
```

---

## 📊 Video Description Prompt Scores

| Prompt | Accuracy | Relevance | Clarity | Tone | Completeness | Total |
|---|---|---|---|---|---|---|
| P1 With Audio | 5 | 5 | 5 | 5 | 5 | 25/25 |
| P2 Without Audio | 5 | 5 | 5 | 4 | 5 | 24/25 |
| P3 Event Caption | 4 | 5 | 5 | 5 | 4 | 23/25 |
| P4 Metadata | 5 | 5 | 4 | 5 | 5 | 24/25 |
| P5 Comparison | 5 | 5 | 5 | 5 | 5 | 25/25 |

**Average: 24.2/25**

---

## 💡 Key Insight

> Video description prompts require **temporal awareness** — describing not just *what* 
> is happening, but *when* and *in what order*. Prompts that include timestamps or 
> sequence markers in the input produce significantly better-structured outputs.
> 
> The WITH AUDIO vs WITHOUT AUDIO distinction is critical:
> - **With audio:** Describe what sound *means* emotionally
> - **Without audio:** Infer emotion from visual cues and flag uncertainties
