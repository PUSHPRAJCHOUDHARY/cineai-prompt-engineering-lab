# 💬 Conversational Prompts

> **Goal:** Design prompts that simulate natural, helpful, multi-turn conversations between a user and an AI assistant in the cinema domain.

---

## What Are Conversational Prompts?

Conversational prompts mimic real dialogue. They require the AI to:
- Understand context from previous messages
- Respond in a natural, friendly tone
- Stay on-topic across multiple exchanges
- Handle follow-up questions gracefully

---

## Prompt 1 — Basic Movie Recommendation

### ❌ Weak Prompt (Version 1)
```
Suggest a movie.
```
**Problem:** No context, no preference, no format — output will be random and unhelpful.

---

### ✅ Strong Prompt (Version 2)
```
You are a friendly movie recommendation assistant. 
The user enjoys thriller movies with psychological depth and plot twists, 
similar to movies like "Gone Girl" and "Shutter Island".

Recommend 3 movies with:
- Movie title and year
- One-line reason why it matches their taste
- Mood rating (Light / Medium / Intense)

Keep the tone conversational and enthusiastic.
```

**Why it works:** Role defined, preferences given, output format specified, tone instructed.

---

## Prompt 2 — Plot Explanation Chat

### ❌ Weak Prompt
```
Explain Inception's plot.
```

### ✅ Strong Prompt
```
You are a patient movie guide assistant helping a first-time viewer 
who just finished watching "Inception" (2010) and is confused.

Explain the plot in simple language without spoiling future plot points.
Use an analogy to everyday life to explain the concept of dream layers.
End with 2 questions the user can think about to understand the movie deeper.
Keep the response under 200 words.
```

---

## Prompt 3 — Actor Career Discussion

### ❌ Weak Prompt
```
Tell me about Joaquin Phoenix.
```

### ✅ Strong Prompt
```
You are a knowledgeable cinema assistant having a casual conversation with a film student.

The student asks: "What makes Joaquin Phoenix different from other actors of his generation?"

Respond conversationally (not like a Wikipedia article).
Mention 2-3 specific performances as evidence.
End your response with a follow-up question to keep the conversation going.
Limit to 150 words.
```

---

## Prompt 4 — Handling an Ambiguous User Question

### ❌ Weak Prompt
```
What happened at the end?
```

### ✅ Strong Prompt
```
You are a movie discussion assistant. A user asks: "What happened at the end?"
but has not mentioned which movie they're referring to.

Do NOT assume which movie they mean.
Politely ask a clarifying question to identify:
1. The movie title
2. Whether they want a factual summary or an interpretation

Keep the tone friendly and curious.
```

**Key Skill Demonstrated:** Handling ambiguous input gracefully — critical for real AI systems.

---

## Prompt 5 — Multi-Turn Conversation Simulation

### Full Conversation Prompt Chain
```
[TURN 1 - User]
I just watched a really sad movie and I don't know how to feel. It was about a father 
losing his child. Can you recommend something lighter to watch next?

[TURN 1 - AI Instruction]
You are an empathetic movie assistant. Acknowledge the user's emotion first (1 sentence), 
then suggest 2 light-hearted feel-good movies. Keep tone warm and gentle.

---

[TURN 2 - User]
Do either of those have any sad parts? I really can't handle more sadness tonight.

[TURN 2 - AI Instruction]
Refer back to the movies you recommended in Turn 1.
For each, give an honest 1-sentence sadness warning (or "completely safe" if none).
Maintain the warm, supportive tone.

---

[TURN 3 - User]
Okay I'll watch the second one. What snacks go well with that kind of movie?

[TURN 3 - AI Instruction]
Step outside pure movie content gracefully.
Give 3 fun snack suggestions with playful one-line descriptions.
End with an encouraging send-off line.
```

**Skill Demonstrated:** Maintaining context across turns, tone consistency, graceful topic transitions.

---

## 📊 Conversational Prompt Scores

| Prompt | Accuracy | Relevance | Clarity | Tone | Completeness | Total |
|---|---|---|---|---|---|---|
| P1 Weak | 3 | 2 | 3 | 3 | 2 | 13/25 |
| P1 Strong | 5 | 5 | 5 | 5 | 4 | 24/25 |
| P2 Strong | 5 | 5 | 5 | 4 | 4 | 23/25 |
| P3 Strong | 4 | 5 | 5 | 5 | 4 | 23/25 |
| P4 Strong | 5 | 5 | 4 | 5 | 5 | 24/25 |
| P5 Strong | 5 | 5 | 5 | 5 | 5 | 25/25 |

**Average (Strong Prompts): 23.8/25**
