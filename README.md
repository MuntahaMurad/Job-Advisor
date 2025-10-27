# AI‑Job‑Advisor

> An AI‑powered system that helps candidates and recruiters make better decisions across the hiring journey.

<p align="center">
  <img src="logo.jpg" alt="AI‑Job‑Advisor Logo" width="220">
</p>

---

## Overview

AI‑Job‑Advisor brings together three complementary capabilities in one workflow:

- **Resume Ranking** — Analyze a candidate’s resume against a target job description (JD) and produce a relevance score with strengths, gaps, and concrete improvement tips.
- **CV Generation / Tailoring** — Draft or tailor a role‑specific CV from an existing resume and the JD, aligning language to required skills and outcomes.
- **Interactive Web App** — A lightweight interface where users upload a resume and JD, view scores/explanations, and (optionally) generate a refined CV.

<p align="center">
  <video width="600" controls>
    <source src="demo-video.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</p>

---

## How It Works (Conceptual)

1. **Ingestion & Normalization** — Parse resumes/JDs into structured sections (skills, tools, experience, education).
2. **Representation** — Convert text into model‑friendly representations (feature sets, embeddings, or prompt‑engineered summaries).
3. **Matching & Scoring** — Compare candidate signals with JD signals; output a **match score**, highlights of overlaps/gaps, and red‑yellow‑green flags.
4. **Advisory Generation** — Use LLM‑style prompts to generate candidate‑facing guidance (missing skills, phrasing improvements, targeted bullets).
5. **User Experience** — The web app surfaces upload, ranking results, explanations, and tailored CV drafts.

---

## Repository Layout (at a glance)

```
resume ranking/   # Parsing, feature extraction, and ranking logic (notebooks & scripts)
cv gen/           # Assets and notebooks for CV drafting/tailoring
web-app/          # Front-end code to interact with models (upload, scoring, CV generation)
logo.jpg          # Project logo
demo-video.mp4    # Short demo clip
```

---

## Typical Use Cases

- **For recruiters:** Quickly shortlist candidates for a role with transparent explanations and consistent criteria.
- **For candidates:** Diagnose gaps against a JD and generate a targeted CV version aligned to the role.

---

## Design Principles

- **Transparency first** — Provide rationales for scores and suggestions.
- **Separation of concerns** — Modeling/evaluation in notebooks; interaction in a small web app; content generation in CV tooling.
- **Experiment‑driven** — Heavy use of notebooks reflects an iterative approach to refining features, prompts, and scoring criteria.

---

## Considerations & Ethics

- **Data quality:** Parsing imperfect resumes/JDs can introduce noise; clean formatting improves outcomes.
- **Bias & fairness:** Any automated screening must be audited and paired with human oversight.
- **Grounding & honesty:** CV generation should remain faithful to the candidate’s true history.

---

## Acknowledgements

This repository combines notebook‑driven experimentation with a simple UI to make AI‑assisted hiring workflows easier to explore and evaluate.
