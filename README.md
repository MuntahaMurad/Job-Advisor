# AI‑Job‑Advisor

An AI‑powered system to help both candidates and recruiters make better decisions across the hiring journey.

---

## What This Project Does

This project brings together three inter‑linked capabilities in one unified workflow:

-   **Resume Ranking**: The system analyzes uploaded candidate resumes against a given job description (JD) and computes a relevance score. Beyond ranking, it explains strengths, gaps, and improvement suggestions.
-   **CV Generation / Tailoring**: Given a candidate’s current CV and a target role/JD, the system produces a tailored draft of the CV (or targeted bullet‑point suggestions) aligned with the job.
-   **Interactive Web Interface**: A minimal web application lets users upload a JD + resume, view scores and insights, and optionally generate a revised CV.

---

## Core Concepts & Workflow

1. **Document Ingestion & Normalization**Resumes and JDs (PDFs, Docs, text) are parsed and segmented into structured parts (skills, experience, education, tools).
2. **Representation & Matching**The content is converted into model‑friendly formats (e.g., embeddings or engineered features). The system compares candidate signals with job signals and outputs a match score, gap analysis, and rationale.
3. **Advisory Generation**Using large language models or prompt‑engineered techniques, the system generates user‑facing feedback such as:
    - “You’re missing skill X for this role”
    - “Your bullet point on Project Y could re‑phrase to emphasise outcome”
4. **User Experience**
   Through the web front end, users upload materials, receive instant alignment scores, view personalised feedback, and (for candidates) download tailored CV versions.

---

## Repository Structure

```
resume ranking/
    Notebooks and scripts for parsing, feature extraction and ranking logic
cv gen/
    Assets and notebooks dedicated to CV generation and tailoring for roles
web‑app/
    Front‑end code to interact with the system (upload, view results, generate CV)
```

---

## Why It Matters

-   **For Recruiters**: Enables faster, more consistent short‑listing of candidates with transparent explanations.
-   **For Candidates**: Helps you understand where you fall short for a target role and how to improve your CV language to match the job.
-   **Duplicable Workflow**: The separation of modelling, generation and UI components makes it easy to adapt the system for different roles, industries or jurisdictions.

---

## Design Philosophy

-   **Transparency**: Rather than a “black‑box score”, each recommendation is explained so users understand _what_ matched and _why_.
-   **Modularity**: Model logic (notebooks) is separated from user interface code (web‑app), making the system easier to iterate and maintain.
-   **Experiment‑driven**: Heavy use of notebooks indicates a research‑first workflow—tune features, prompts, ranking criteria then deploy into UI.

---

## Limitations & Considerations

-   **Parsing Quality**: Inaccurate extraction (poorly formatted resumes/JDs) will impact alignment quality.
-   **Bias & Ethics**: Automated ranking must be audited for fairness, avoiding unintended bias in short‑listing.
-   **CV Honesty**: Tailored CVs should always reflect the candidate’s true experience and not mislead.
