---
name: academic-prompt-codes
description: >-
  Master framework of Academic Prompt Codes (L99, ULTRATHINK, FIRSTPRINCIPLES, OODA,
  /premortem, GAPFINDER, /skeptic, /devil, /brutal, REDTEAM, /steelman, /blindspots,
  ALT4, /ghost, /punch, /truth, cite-or-flag), 7-Layer Prompt Structure, CO-STAR/RISEN/CRAFT
  frameworks, Power Combos, and Subagent Orchestration rules distilled from
  Prof. Somkiat Wattanasirichaigoon's ResearchPrompt.pdf. Use when executing prompt codes,
  orchestrating specialized research subagents, or designing multi-agent academic workflows.
---

# Academic Prompt Codes & Subagent Orchestration Skill

Distilled from **`skill/ResearchPrompt.pdf`** (*Prompt Codes for Academic Excellence: IT Management Graduate Program*, Prof. Somkiat Wattanasirichaigoon, M.D., Expert Reviewer, NRCT).

## 1. Core Principle: AI as a Controlled Information System (Slide 3)

Every research task or subagent invocation must follow the **4-Stage IS Control Loop**:
1. **Input:** Project context (`README.md`), attached primary documents (`literature/pdfs/`, `journal/library.bib`), and explicit Role (`/role`).
2. **Process:** AI Model + **Prompt Codes** that govern cognitive depth, analytical framing, and critique.
3. **Output:** Grant proposal sections, Q1 manuscript chapters (`.tex` $\rightarrow$ `journal/journal.pdf`), Markdown paper notes (`note.md`), IRB packages, or patent claims *(all `.html` summaries and `journal-th.pdf` are suspended / on-demand only per `AGENTS.md` §2.14)*.
4. **Control:** Fact-checking (`/truth`), internal consistency verification (`/verify`), source verification (`cite-or-flag`), and ethical compliance.

---

## 2. The 7-Layer Prompt Architecture (Slide 10)

Structure complex prompts and subagent instructions using these 7 layers in order:

| Layer | Code | Function | Example in Ph.D. / Q1 Research |
| :---: | :--- | :--- | :--- |
| **1** | `/role` | Define expert persona | Senior AIS Basket Q1 Editor / 20-Year NRCT Reviewer / IRB Methodologist |
| **2** | `/objective` | State primary deliverable | Draft or critique a submission-ready Q1 manuscript section or grant module |
| **3** | `/context` | Supply domain & files | Target journal, stakeholder strata, attached `<documents>...</documents>` |
| **4** | `/constraints` | Hard boundaries | Use only verified sources in `journal/library.bib`; never invent citations or stats |
| **5** | `/format` | Output specification | LaTeX (`.tex`) or structured Markdown matrix *(no `.html` summaries unless explicitly requested)* |
| **6** | `/verify` | Pre-delivery audit | Verify alignment across Research Questions $\leftrightarrow$ Objectives $\leftrightarrow$ Methods $\leftrightarrow$ Hypotheses |
| **7** | `/final-only` | Clean output mode | Deliver the publication-ready artifact directly without conversational filler |

### Complementary Global Frameworks (Slide 11)
- **CO-STAR** (`Context · Objective · Style · Tone · Audience · Response`): Best for **Abstracts, Cover Letters to Editors, and Executive Summaries**.
- **RISEN** (`Role · Instructions · Steps · End goal · Narrowing`): Best for **Research Methodology (Chapter 3), PLS-SEM/MGA protocols, and multi-stage workflows**.
- **CRAFT** (`Context · Role · Action · Format · Target audience`): Best for **rapid daily research tasks and targeted revisions**.

---

## 3. The 6 Prompt Code Groups (Slides 12–18)

When the user types any of these codes (or when dispatching a subagent), execute the exact cognitive behavior defined below:

### Group 1: Depth of Thinking (ความลึกของการคิด — Slide 12)
- **`L99`**: Expert-level depth and committed judgment ("ฟันธง ไม่กั๊ก"). Lead with the verdict, state mechanisms and boundary conditions, and calibrate confidence.
- **`ULTRATHINK`**: Maximum multi-dimensional reasoning before generating output; trace second- and third-order theoretical and empirical consequences.
- **`/deep`**: Drill beneath surface descriptions into underlying causal mechanisms, mathematical specifications, and institutional micro-foundations.
- **`META`**: Analyze the structural logic and meta-theoretical assumptions of the prompt/problem before answering.
- **`CHAINLOGIC`**: Explicitly link every premise in a step-by-step causal chain ($A \rightarrow B \rightarrow C$) with zero logical leaps.
- **`FIRSTPRINCIPLES`**: Deconstruct the research problem down to foundational axioms rather than copying conventional templates. *(Use for Chapter 1 Introduction & Theoretical Problematization).*

### Group 2: Analysis & Decision Making (วิเคราะห์และตัดสินใจ — Slides 13 & 18)
- **`OODA`** (*Observe $\rightarrow$ Orient $\rightarrow$ Decide $\rightarrow$ Act*):
  1. *Observe:* List raw empirical/project facts and resource constraints.
  2. *Orient:* Interpret facts within the institutional/disciplinary context (the decisive step ★).
  3. *Decide:* Commit to the single best strategic option.
  4. *Act:* Specify a concrete, time-bound action plan.
- **`/premortem`**: Assume the manuscript was desk-rejected or the grant/fieldwork failed 6 months from now; work backward to identify the top fatal causes and fix them preemptively.
- **`INVERT`**: Work backward from the target end-state (e.g., Q1 acceptance in *GIQ* or 5–10 year national AI capability) to required prerequisites.
- **`PARETO`**: Identify the vital 20% of constructs, arguments, or methodological fixes that drive 80% of reviewer acceptance.
- **`/swot`**: Structured Strengths, Weaknesses, Opportunities, and Threats matrix.
- **`WARGAME`**: Simulate how rival theoretical camps, competing grant applicants, or hostile stakeholders will counter-mobilize.
- **`ALT4`**: Generate 4 distinct, well-justified strategic alternatives (e.g., 4 manuscript titles, 4 rival explanations, 4 future research directions, or 4 prior-art keyword sets) from a single prompt.
- **`XRAY`**: Strip away jargon to expose the core structural bottleneck of the problem.

### Group 3: Blindspots & Adversarial Critique (หาจุดบอดและวิจารณ์ — Slide 14)
- **`/skeptic`**: Question every unstated assumption, causal claim, and operationalization.
- **`/devil`**: Argue forcefully from the opposing theoretical or empirical viewpoint (e.g., offer 3 rival explanations for an observed effect).
- **`/brutal`**: Deliver candid, unvarnished peer-review criticism without sugarcoating ("วิจารณ์ตรง ไม่ถนอมน้ำใจ").
- **`REDTEAM`**: Append at the end of a prompt to audit the output for logical flaws, validity threats, and severity-ranked limitations.
- **`/steelman`**: Construct the strongest possible version of a rival theory before refuting or integrating it. *(Essential for Chapter 2 & Discussion).*
- **`/blindspots`**: Uncover hidden methodological, sampling, or theoretical blindspots that the author overlooked.
- **`GAPFINDER`**: Identify 3 concrete research gaps from attached literature and formulate 1 **FINER** (*Feasible, Interesting, Novel, Ethical, Relevant*) research question per gap.
- **`ANTIADVISE`**: Diagnose "If we wanted to guarantee this study gets desk-rejected, what mistakes would we make?"—then invert to safeguard the manuscript.

### Group 4: Creativity & Synthesis (ความคิดสร้างสรรค์ — Slide 15)
- **`/opposite`**: Invert conventional wisdom (e.g., showing how construct X can reduce rather than increase outcome Y under specific countervailing mechanisms).
- **`/diverge`**: Expand the conceptual space as widely as possible before filtering.
- **`/combine`**: Synthesize constructs across disciplines (e.g., integrating theoretical lenses across reference disciplines such as Information Systems, Strategic Management, and Institutional Theory).
- **`/brainstorm`**: High-volume ideation.
- **`UNLEARN`**: Discard stale textbook clichés (e.g., generic TAM/UTAUT extensions) and propose fresh theoretical mechanisms.
- **`LINDYMODE`**: Anchor arguments in time-tested foundational classics of relevant reference disciplines rather than ephemeral buzzwords.
- **Recommended Creative Pipeline:** `/diverge` $\rightarrow$ `/combine` $\rightarrow$ `/skeptic` (Expand $\rightarrow$ Synthesize $\rightarrow$ Filter).

### Group 5: Format & Prose Style (รูปแบบและสำนวน — Slide 16)
- **`/tldr`**: Ultra-concise executive summary.
- **`ELI10`**: Explain complex statistical or theoretical mechanisms in plain, intuitive language.
- **`/HUMAN`**: Natural, authoritative human academic prose.
- **`/ghost`**: Strip all AI-sounding filler words (*"delve", "pivotal", "groundbreaking", "in today's fast-paced world", "it is important to note"*).
- **`/punch`**: High-impact, tight, economical sentences.
- **`/noyap`**: Zero preamble, zero meta-commentary; start immediately with the substantive content.
- **`/table`**: Present comparisons, synthesis matrices, or rubric evaluations in structured tables.
- **`/final-only`**: Output only the final copy-ready text or code.

### Group 6: Accuracy & Anti-Hallucination (ความถูกต้อง ลดการแต่งข้อมูล — Slide 17)
- **`/truth`**: Never guess or fabricate facts, DOIs, page numbers, or statistics; state `"cannot be verified"` if evidence is absent.
- **`/verify`**: Cross-check internal consistency across RQs, hypotheses ($H_1$, $H_2$, ...), equations, survey items, and citations before responding.
- **`Ask me questions`**: Pause and ask up to 3 clarifying questions when ambiguity would alter the deliverable.
- **`/assumptions`**: Explicitly list all assumptions made in the analysis.
- **`Confidence`**: Tag every major claim or verdict with **High / Medium / Low confidence** and state what evidence would change the call.
- **`cite-or-flag`**: Every factual or theoretical claim must cite a verified source (`[Author, Year, p. X]`) or be explicitly flagged with **`[ต้องตรวจ / NEEDS VERIFICATION]`**.

---

## 4. High-Impact Power Combos (Slide 19 & Slide 43)

Rule of thumb: **Use at most 3 codes per prompt — place Depth/Analysis codes at the front, and Format/Verification codes at the end.**

| Power Combo | Use Case | Behavior |
| :--- | :--- | :--- |
| **`L99 + /premortem`** | Grant proposals & research designs | Deep expert architecture + preemptive diagnosis of fatal rejection risks |
| **`OODA + L99`** | Strategic research planning | Observe-Orient-Decide-Act loop ending in a decisive, time-bound action plan |
| **`OODA + /brutal`** | Feasibility & progress audit | Unvarnished assessment of current bottlenecks and immediate corrective actions |
| **`/skeptic + ULTRATHINK`** | High-stakes theoretical modeling | Deep multi-order reasoning that stress-tests every causal path and boundary condition |
| **`/steelman + /verify`** | Academic manuscript drafting | Strongest engagement with rival theories + strict RQ-method-result alignment |
| **`/role + /verify + /final-only`** | Formal submission documents | Persona-calibrated, internally verified, ready-to-submit LaTeX/HTML output |
| **`/ghost + /punch`** | Cover letters, abstracts, emails | Zero AI clichés, crisp high-impact academic prose |

---

## 5. Subagent Spawning Playbook for Q1 Journal Research (`define_subagent` / `invoke_subagent`)

When decomposing a Q1 journal research workflow into parallel or sequential subagents, equip each subagent with its corresponding specialized skill in `.agents/skills/`:

1. **`q1-manuscript-redteam` Subagent** (`.agents/skills/q1-manuscript-redteam/SKILL.md`):
   - **Role:** `Q1 Journal Editor & Reviewer-2 Red Team`
   - **Default Codes:** `L99 + /steelman + /brutal + /blindspots + /verify + cite-or-flag`
   - **Tasks:** IMRaD section drafting/auditing, Literature Synthesis Matrix, Rival Explanations (`/devil REDTEAM`), Severity-Ranked Limitations, Title/Abstract/Cover Letter (`ALT4`, `/ghost + /punch`), Reviewer-2 Simulation (`3 Major + 5 Minor`), and Point-by-Point Response Letter table.
2. **`literature-review-synthesizer` Subagent** (`.agents/skills/literature_review_synthesizer/SKILL.md`):
   - **Role:** `Senior IS Literature Review Synthesizer`
   - **Default Codes:** `L99 + /combine + /steelman + /table + /truth + cite-or-flag`
   - **Tasks:** Thematic synthesis across verified Q1 papers (`journal/library.bib` and `literature/`), Concept Matrix construction, and FINER research gap identification (`GAPFINDER /skeptic`).
3. **`research-background-writer` Subagent** (`.agents/skills/research_background_writer/SKILL.md`):
   - **Role:** `Q1 Chapter 1 Problematization & Funnel Architect`
   - **Default Codes:** `L99 + FIRSTPRINCIPLES + /skeptic + /ghost + /punch`
   - **Tasks:** Macro $\rightarrow$ Meso $\rightarrow$ Micro background drafting, Alvesson & Sandberg (2011) assumption problematization, and Type III error testing (Rai, 2017).

---

## 6. Substantive Research Logging Standard (`AGENTS.md` §2.11)
When concluding any research workflow, append to `.log/research-log.md`, `irb/AI_USE_LOG.md`, and `TODO.md` (under `# LOG`) **ONLY substantive research milestones and research modifications** (theoretical mechanisms, model specifications, scale psychometrics, empirical findings, literature matrices, statistical tests, and Reviewer-2 critiques).
**STRICTLY FORBIDDEN IN LOGS:** Operational workspace context, file/folder renaming (e.g. renaming deliverables), HTML UI formatting, CSS edits, LaTeX math cleansing in HTML tags, git actions, skill script maintenance, or temporary file generation/deletion.


