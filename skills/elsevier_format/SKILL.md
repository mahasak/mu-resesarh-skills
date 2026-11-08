---
name: elsevier_format
description: >-
  Applies Elsevier general manuscript formatting guidelines (Submission 101) for
  academic papers: title page placement, 150-250 word self-contained abstract
  without references or abbreviations, one-inch margins on all sides throughout the document,
  left-aligned body text starting on a new page, and top-of-page centered references
  with author-year (Surname, Year) or numbered citation styling.
  https://scientific-publishing.webshop.elsevier.com/manuscript-preparation/what-submission-format-should-use-academic-papers/
---

# Skill: Elsevier Manuscript Formatting Standard (`elsevier_format`)

## Description
This skill codifies and enforces the universal academic manuscript formatting standard established by Elsevier's *Submission 101: What format should be used for academic papers?* (Elsevier Webshop / Author Services). It serves as the authoritative blueprint for preparing, auditing, and restructuring academic manuscripts prior to journal submission.

---

## Core Specifications & Formatting Rules

### 1. Title Page
The title page is the manuscript's initial impression and must follow precise architectural placement:
* **Placement:** The title must be placed strictly in the **upper half** of the title page.
* **Alignment:** Centered horizontally.
* **Capitalization:** **Title Case** (capitalize the first letter of all principal words; lowercase minor grammatical particles such as "and," "or," "of," "in," "for," "with," "to," "a," "an," "the," unless they begin the title or subtitle).
* **Metadata Hierarchy:** Author name(s), institutional affiliations, corresponding email, and target outlet clearly demarcated in the lower half of the page.
* **Pagination:** Title page stands alone or separates cleanly before the abstract.

### 2. Abstract
The abstract delivers a concise, standalone synthesis of the study:
* **Core Dimensions Covered:** Aims / Background & Problem, Theoretical Grounding, Methodological Design, Findings / Expected Contribution, and Practical / Policy Significance.
* **Content Constraints:**
  - **Self-contained:** Must make complete sense without reading the full article.
  - **Zero References:** Strictly free of bibliographic citations (`\cite`, `\citep`, author-year references).
  - **Zero Unexpanded Abbreviations / Latent Codes:** Free of acronyms or construct variable abbreviations (e.g., write out "Perceived Policy Necessity" rather than `NEC`; write out "Structural Equation Modeling" upon first mention).
  - **Zero Footnotes:** No footnotes or marginal notes.
* **Length:** Strict word count constraint of **150–250 words** (never exceeding 250 words).
* **Keywords:** Immediately following the abstract, providing 5–8 standardized indexing keywords.

### 3. Main Body Text & Margins
Consistency, reader navigability, and strict page geometry govern the manuscript body:
* **Margins:** Ensure you leave a **one-inch margin on all sides** (top, bottom, left, and right: 1 in / 2.54 cm / 72.27 pt) throughout the entire document via `\usepackage[margin=1in]{geometry}`.
* **Layout Transition:** The main body **MUST begin on a new page** (`\clearpage` / `\newpage`) immediately following the abstract.
* **Font Consistency:** A single uniform font family must be used throughout the entire paper (e.g., Times Roman via `newtxtext,newtxmath`).
* **Text Alignment:** All main body paragraphs must be **aligned to the left** (`\raggedright` or `\RaggedRight` with proper hyphenation, or left-justified standard margins without ragged right irregularities).
* **Spacing & Indentation:** Paragraph spacing and indentation must remain strictly consistent throughout all chapters and subsections.
* **Headings:** Clearly delineated heading hierarchy (Numbered Sections, Subsections, Subsubsections).
* **In-text Citation:** Use format "Surname, Year" only, Example: `(Smith, 2023)` or `Smith (2023)`.

### 4. "References" Section
Bibliographic references must adhere to structured submission rules:
* **Heading Placement:** The section must begin with the word **“References”** placed at the **top of the page** (preceded by a page break `\clearpage`) and **centered**.
* **List Alignment:** For the reference entries themselves, use **left-aligned text** (`\raggedright`) to avoid awkward justification gaps with URLs, DOIs, and long titles.
* **Citation & Reference Styles:**
  - **Author-Year / APA 7 (Standard for IS/Management Journals, e.g., GIQ, IJIM, JSIS):** In-text citations use "Surname, Year" only (`(Smith, 2023)` or `Smith (2023)`). Reference entries are alphabetical by author surname, unnumbered, with hanging indentation and left alignment (`elsarticle-harv.bst`).
  - **Numbered Style (for specific technical journals requiring sequential citations):** Sequential numbers (`[1]`, `[2]`, `[1–3]`) matching numbered reference list entries via `elsarticle-num.bst`.

### 5. Floats, Tables, and Figures
* **Placement:** Full-width single-column floats (`table*`, `figure*`) for complex analytical models and multi-column tables.
* **Captions:** Self-contained, placed above tables and below figures.
* **Spacing in Floats:** Single-spaced inside tabular environments for visual compactness.

---

## LaTeX Implementation Reference

```latex
% --- Elsevier Submission 101 Typography & Layout ---
\documentclass[10pt,a4paper]{article}
\usepackage{newtxtext,newtxmath}       % Single uniform font: Times
\usepackage[margin=1in]{geometry}       % Strictly 1-inch margins on all sides throughout
\usepackage{setspace}                   % Line spacing control
\usepackage{ragged2e}                   % Left alignment with hyphenation: \RaggedRight

% --- Citation System (Author-Year: Surname, Year) ---
\usepackage[authoryear,round]{natbib}   % Format: (Surname, Year)
% Alternative for Numbered Outlets: \usepackage[numbers,sort&compress]{natbib}

% --- Centered References Heading Hook ---
\renewcommand\bibsection{\clearpage\twocolumn[\begin{center}{\Large\bfseries References\par}\vspace{1.5em}\end{center}]}
\renewcommand\bibfont{\raggedright}

% --- Title Page Environment ---
\begin{titlepage}
\begin{center}
    \vspace*{2.0cm}
    {\huge\bfseries Title Written in Title Case\par}
    \vspace{1.5cm}
    {\LARGE\bfseries Author Name\par}
    \large Doctoral Candidate / Affiliation\par
    \vfill
    {\normalsize Target Outlet / Date\par}
    \vspace*{1.0cm}
\end{center}
\end{titlepage}

% --- Abstract Page ---
\clearpage
\begin{center}
    {\Large\bfseries Abstract\par}
\end{center}
\begin{spacing}{1.0}
% Self-contained, 150-250 words, NO citations, NO abbreviations
[Abstract text: 150-250 words]

\vspace{1.0em}
\noindent\textbf{Keywords:} Keyword 1, Keyword 2, Keyword 3, Keyword 4, Keyword 5.
\end{spacing}

% --- Main Body Starts on a New Page ---
\clearpage
\twocolumn % or \onecolumn per journal requirements
\RaggedRight % Left-aligned body text
\section{Introduction}
...

% --- References Starts on a New Page, Centered Heading, Left-Aligned Entries ---
\clearpage
\bibliographystyle{elsarticle-harv} % or elsarticle-num for numbered journals
\bibliography{library}
```

---

## Verification & Audit Checklist

When auditing or applying this skill to a manuscript, verify:
- [ ] **Title Page:** Title in upper half, centered, formatted strictly in Title Case.
- [ ] **Abstract:** Exactly 150–250 words. 0 citations (`\cite`), 0 unexpanded construct codes/acronyms, 0 footnotes.
- [ ] **Margins:** Ensure a one-inch (1-in / 2.54 cm / 72.27 pt) margin on all sides (top, bottom, left, right) throughout the entire document (`\usepackage[margin=1in]{geometry}`).
- [ ] **Main Body Start:** Begins on a fresh page directly following abstract (`\clearpage`).
- [ ] **Font:** Single uniform font across text and math (e.g. Times Roman).
- [ ] **In-text Citation:** Formatted strictly as "Surname, Year" only, e.g., `(Smith, 2023)`.
- [ ] **References Heading:** Starts at the top of a page (`\clearpage`), word "References" is centered.
- [ ] **Reference Entries:** Arranged alphabetically, hanging indentation, left-aligned (`\raggedright`), with DOIs.
