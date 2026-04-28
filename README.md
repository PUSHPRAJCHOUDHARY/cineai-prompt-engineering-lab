# 🎬 CineAI Prompt Engineering Lab

> **A complete Prompt Engineering project covering Conversational, Generative, Descriptive, Image Caption, Video Description prompts — with Evaluation, Scoring, and Iterative Refinement.**

---

## 📌 Project Overview

This project demonstrates end-to-end prompt engineering skills applied to a **cinema/entertainment AI assistant** use case.

The goal was to design, test, evaluate, and refine prompts across **5 major prompt categories** used in real-world AI systems — directly aligned with industry requirements for Prompt Engineering roles.

All prompts were tested using **ChatGPT (GPT-4)** and evaluated using a custom **5-dimension scoring rubric**.

---

## 🎯 Why This Use Case?

Cinema content is rich with diverse data types:
- Visual scenes → Image captions
- Trailers/clips → Video descriptions
- Plot discussions → Conversational prompts
- Story generation → Generative prompts
- Scene breakdown → Descriptive prompts

This makes it a perfect sandbox for practicing **all core prompt types** in one unified domain.

---

## 📁 Project Structure

```
prompt-engineering-project/
│
├── prompts/
│   ├── 01_conversational_prompts.md     # Chat-style Q&A prompts
│   ├── 02_generative_prompts.md         # Creative content generation
│   ├── 03_descriptive_prompts.md        # Detailed scene/event descriptions
│   ├── 04_image_caption_prompts.md      # Captions for movie stills/posters
│   └── 05_video_description_prompts.md  # Video summaries with/without audio
│
├── evaluation/
│   ├── scoring_rubric.md                # 5-dimension evaluation framework
│   └── prompt_evaluation_sheet.md       # Scored results for all 25 prompts
│
├── refinement/
│   └── before_after_examples.md         # 10 prompt refinement case studies
│
├── outputs/
│   └── key_insights.md                  # Findings, patterns, and learnings
│
└── README.md
```

---

## 🔢 Prompt Count Summary

| Category | No. of Prompts |
|---|---|
| Conversational | 5 |
| Generative | 5 |
| Descriptive | 5 |
| Image Caption | 5 |
| Video Description | 5 |
| **Total** | **25 Prompts** |

---

## 📊 Evaluation Dimensions

Every prompt-response pair was scored on:

| Dimension | What it Measures |
|---|---|
| Accuracy | Is the information factually correct? |
| Relevance | Does it answer what was asked? |
| Clarity | Is it easy to understand? |
| Tone | Is the tone appropriate for the context? |
| Completeness | Does it cover all aspects of the prompt? |

**Score scale: 1–5 per dimension → Max 25 points per prompt**

---

## 🔑 Key Findings

- Zero-shot prompts scored avg **16.2/25** — decent but inconsistent
- Adding **role + context + format instructions** pushed scores to avg **22.4/25**
- Prompts with **explicit output format** (bullet/paragraph/numbered) were scored 31% higher on Clarity
- Video description prompts without audio cues needed **more sensory language instructions**
- Conversational prompts improved significantly when **persona framing** was added

---

## 🛠️ Tools Used

- **LLM:** ChatGPT (GPT-4o)
- **Evaluation:** Custom rubric (designed from scratch)
- **Documentation:** Markdown
- **Version tracking:** GitHub

---

## 👤 Author

**Pushpraj Choudhary**
- 📧 pushprajchoudhary6261880542@gmail.com
- 🔗 [LinkedIn](#)
- 📍 Bhopal, India

---

## 💡 What I Learned

1. Prompt structure matters more than prompt length
2. Specificity always outperforms vagueness
3. Iterative refinement is not optional — it's the core skill
4. Evaluation without a rubric is just opinion — scoring makes it measurable
5. The same task phrased 3 different ways can produce 3 very different quality outputs
