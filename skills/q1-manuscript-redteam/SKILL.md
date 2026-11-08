---
name: q1-manuscript-redteam
description: >-
  Specialized workflow for Q1 academic manuscript engineering, IMRaD section drafting,
  journal scope matching, Literature Synthesis Matrix, Discussion rival explanations,
  Reviewer-2 Red-Team simulation (3 Major + 5 Minor critiques), and Point-by-Point
  Response Letters using academic prompt codes. Use when drafting, auditing, or
  red-teaming journal manuscripts or spawning a Reviewer-2 / Editor subagent.
---

# Q1 Manuscript Engineering & Reviewer-2 Red-Team Skill

Distilled from **Section C (Slides 28–34)** of `skill/ResearchPrompt.pdf` (*Prompt Codes for Academic Excellence*, Prof. Somkiat Wattanasirichaigoon, M.D.) and integrated with `AGENTS.md` L99 Q1 standards.

## When to Use This Skill (or Spawn as a Subagent)
> **On-Demand Execution Guardrail:** Workflows 1 (`journal_review.html` / Target Journal Fit) and 4 (`manuscript-redteam.html` / Reviewer-2 Red-Team Simulation) are strictly **ON-DEMAND ONLY**. NEVER auto-summarize `journal_review.html` or auto-run/update `manuscript-redteam.html` during routine manuscript edits unless explicitly requested by the user.

Activate this skill—or instruct a subagent to follow it—whenever performing:
1. Target journal selection & predatory journal screening (Slide 28)
2. IMRaD section drafting or structural auditing (Slide 29)
3. Literature Synthesis Matrix construction from verified PDFs/notes (Slide 30)
4. Discussion rival explanations, severity-ranked limitations, and future research directions (Slide 31)
5. Title, Structured Abstract, ACM CCS / Thesaurus Keywords, and Editor Cover Letter generation (Slide 32)
6. Harsh Reviewer-2 Simulation (`3 Major + 5 Minor`) and Point-by-Point Response Letter drafting (Slide 33)
7. ICMJE / COPE AI Disclosure verification (Slide 34)

---

## Workflow 1: Target Journal Fit & Predatory Audit (Slide 28)
**Prompt Code Formula:** `/role Senior Journal Editor — Compare Abstract against Aims & Scope of 3–5 Candidate Journals /table /verify`

1. Verify every candidate journal in `ranking/quartile-checks.csv` (and `ranking/scimagojr 2025.csv`).
2. Screen out predatory/hijacked journals using **Think. Check. Submit.** criteria:
   - Flag frequent unsolicited spam invitations, abnormally fast guaranteed publication promises, or URLs/ISSNs missing from official Scopus/SJR records.
3. Output a comparison `/table`:
   - `Journal Title & ISSN | SJR 2025 Score & Q1 Category | Aims & Scope Fit with Manuscript | Typical Review Time & APC | Verdict (Reach / Realistic / Fallback)`

---

## Workflow 2: IMRaD Section-Specific Code Execution (Slide 29)

Apply the dedicated Prompt Code pair to each manuscript section:

| Manuscript Section | Mandatory Prompt Codes | Execution Rules |
| :--- | :--- | :--- |
| **1. Introduction** | `FIRSTPRINCIPLES + /skeptic` | Deconstruct the phenomenon from first principles; problematize the underlying assumption of prior literature (Alvesson & Sandberg, 2011) rather than claiming "no one studied X in context Y." |
| **2. Literature Review** | `/role Senior IS Researcher + /table + cite-or-flag` | Execute [`literature-review-synthesizer`](../literature_review_synthesizer/SKILL.md), the single source of truth for the **Literature Synthesis Matrix** (`Study (Year) \| Key Variables/Focus \| Methodology & Sample \| Main Findings \| Limitations/Gaps`), source admission rules, and typed gaps. Use only verified sources; synthesize top 3 cross-study trends. Never write author-by-author laundry lists. |
| **3. Methods** | `/verify + /step-by-step` | Ensure 100% replicability. Every Research Question and Hypothesis must map explicitly to sampling strata, measurement items, and statistical tests (e.g. SEM, measurement invariance, MGA, CMB, endogeneity). |
| **4. Results** | `/table + /constraints` | Report exact test statistics, effect sizes ($f^2$), confidence intervals, and out-of-sample metrics (`PLSpredict`). Strictly forbid over-interpreting beyond the empirical data. |
| **5. Discussion & Limitations** | `/steelman + /devil + REDTEAM + ALT4` | Compare findings against the strongest version of rival theories (`/steelman`); propose **3 alternative explanations** (`/devil`); list **5 limitations ranked by severity** (`REDTEAM`); propose **4 concrete future research directions** (`ALT4`). |

---

## Workflow 3: Title, Abstract, Keywords & Cover Letter (Slide 32)

1. **Title (`ALT4`):** Propose **4 distinct manuscript titles** (e.g., Phenomenon-led, Theory-led, Paradox-led, Method-led) with a 1-sentence rationale for each and recommend the strongest one.
2. **Abstract (`/trim + /punch`):** Write a structured Q1 abstract (*Background/Problem $\rightarrow$ Objective/Theory $\rightarrow$ Method $\rightarrow$ Findings/Contribution*) strictly within the target journal's word limit (typically 150–250 words), with zero filler.
3. **Keywords (`/table`):** Map 5–7 keywords against standard disciplinary taxonomies (e.g., ACM Computing Classification System [CCS] or AIS/Scopus controlled vocabulary).
4. **Cover Letter (`/ghost + /punch`):** Draft a 1-page Cover Letter to the Editor-in-Chief highlighting: (a) why the study's theoretical contribution fits the journal's readership right now, (b) methodological rigor, and (c) originality and ethics compliance—free of AI clichés.

---

## Workflow 4: Two-Stage Reviewer-2 Simulation & Response Letter (Slide 33)

### Stage 1: Simulate the Strict Reviewer (`/role Strict Q1 Reviewer 2 + /brutal + /blindspots`)
Audit the attached manuscript (`.tex` or `.html`) across three independent lenses (*Editor*, *Reviewer 1 [Theory]*, *Reviewer 2 [Methods]*) and output:
- **Desk-Reject Risk Rating:** `High` / `Medium` / `Low`
- **3 Major Critiques (Major Revisions / Fatal Threats):** Deep theoretical, construct-validity, identification, or endogeneity flaws that could trigger rejection.
- **5 Minor Critiques:** Operationalization clarity, boundary conditions, table formatting, citation currency, or prose precision.

### Stage 2: Author the Point-by-Point Response Letter (`/role Professional Academic Author + /table + /verify`)
For every Editor and Reviewer comment, construct a structured Response Table following the **Thank $\rightarrow$ Answer Directly $\rightarrow$ Pinpoint Exact Line/Page Revised** rule:

| Reviewer Comment # | Summary of Critique | Author Response (Concede or Rebut with Evidence) | Exact Manuscript Modification (File, Section, Page/Line, Quoted Revision) |
| :---: | :--- | :--- | :--- |
| `Major 1` | ... | ... | `journal/chapterX.tex` (§X.Y, p. Z) |

---

## Workflow 5: Ethical AI Disclosure Statement (Slide 34)
Verify that `irb/AI_USE_LOG.md` is up to date strictly adhering to the **Substantive Research Logging Standard (`AGENTS.md` §2.11)** (recording exclusively substantive research and writing assistance; strictly excluding operational workspace chores, file renaming, or HTML review formatting) and generate the journal-compliant disclosure statement (per ICMJE / COPE / Elsevier / Taylor & Francis guidelines):
> *"During the preparation of this work, the author(s) used [AI Tool / Model] in order to assist with literature organization, LaTeX formatting, and language refinement. After using this tool/service, the author(s) reviewed and edited the content as needed and take full responsibility for the content of the publication."*
