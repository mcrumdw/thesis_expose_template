# Thesis Exposé Template

An Overleaf-ready LaTeX template for writing an academic thesis exposé at the Faculty of Computer Science, under the supervision of **Prof. Dr. Ignacio Alvarez**.

The template produces a structured, professionally formatted PDF that covers all standard exposé sections: introduction, problem statement, research questions, objectives, related work, methodology, expected contributions, and a Gantt-chart work plan.

---

## Repository Structure

```
thesis_expose_template/
├── expose.tex          # Main LaTeX source — edit this file
├── literature.bib      # Bibliography database — add your references here
├── images/
│   ├── thiRGB.jpg      # Faculty/institution logo (title page)
│   └── statistik1.png  # Example figure
├── expose.pdf          # Pre-compiled PDF preview
├── LICENSE
└── README.md
```

---

## How to Use the Template

### 1. Fill in the Placeholders

Open `expose.tex` and replace every item written in `[SQUARE BRACKETS]` with your own information. Key fields to update:

| Placeholder | Where | What to write |
|---|---|---|
| `[DEGREE PROGRAM]` | Title page | e.g., *Master of Science in Computer Science* |
| `[YOUR THESIS TITLE HERE]` | Title page | Your working thesis title |
| `[Your Full Name]` | Title page & footer | Your first and last name |
| `[XXXXXXXX]` | Title page | Your student ID number |
| `[Supervisor Name]` | Title page | e.g., *Ignacio Alvarez* |
| `[DD.MM.YYYY]` | Title page | Planned submission date |

### 2. Follow the Guidance Notes

Throughout `expose.tex`, teal-coloured `\guidance{...}` blocks appear in the compiled PDF. They explain what to write in each section and offer tips. Once you have written your content, **delete** the corresponding `\guidance{...}` command — it is only scaffolding.

### 3. Add Your References

Edit `literature.bib` and add BibTeX entries for every source you cite. You can export entries directly from Google Scholar, Zotero, or Mendeley. The template uses the `dinat` bibliography style.

### 4. Add Your Own Glossary Terms

Inside `expose.tex`, find the `GLOSSARY ENTRIES` section and add or remove `\newglossaryentry` definitions to match the abbreviations used in your exposé.

### 5. Compile the Document

The template requires a four-step compilation sequence:

```
pdflatex expose.tex
bibtex expose
pdflatex expose.tex
pdflatex expose.tex
```

Overleaf handles this automatically. If compiling locally, make sure you have a full TeX distribution (e.g., TeX Live or MiKTeX) installed.

---

## Importing into Overleaf

### Option A — Upload as a ZIP file (from your computer)

1. Download or clone this repository to your computer.
2. Select all files (`expose.tex`, `literature.bib`, `images/`, etc.) and compress them into a single `.zip` archive. **Do not include the `.git/` folder.**
3. Go to [overleaf.com](https://www.overleaf.com) and log in.
4. On your dashboard, click **New Project → Upload Project**.
5. Drag and drop your `.zip` file (or click to browse to it).
6. Overleaf will extract and open the project automatically. Set the **Main document** to `expose.tex` if prompted.

### Option B — Import directly from GitHub

1. Go to [overleaf.com](https://www.overleaf.com) and log in.
2. On your dashboard, click **New Project → Import from GitHub**.
3. If this is your first time, Overleaf will ask you to link your GitHub account — follow the on-screen instructions.
4. Search for or select the repository **`ignacioalvmar/thesis_expose_template`**.
5. Click **Import to Overleaf**. The project will be created and opened immediately.
6. To pull future updates from GitHub into Overleaf, open the project and go to **Menu → GitHub → Pull changes from GitHub**.

> **Tip:** The GitHub import option keeps your Overleaf project connected to the repository, so you can push and pull changes between both platforms as you work.

---

## Template Sections at a Glance

| # | Section | Suggested Length |
|---|---|---|
| 1 | Introduction and Motivation | 1–2 pages |
| 2 | Problem Statement and Research Questions | 0.5–1 page |
| 3 | Objectives | 0.5 pages |
| 4 | Related Work | 1–2 pages |
| 5 | Methodology | 1–2 pages |
| 6 | Expected Contributions and Results | 0.5–1 page |
| 7 | Work Plan and Schedule (Gantt chart) | 1 page |

---

## Example: Preparing for Your First Topic Discussion with Prof. Dr. Alvarez

Before meeting with your supervisor to discuss your thesis topic, investing time in preparation will make the conversation far more productive and leave a strong first impression. Below is an example preparation guide you can adapt to your own situation.

---

### Preparation Guide — Initial Thesis Topic Meeting

**Goal of the meeting:** Align on a research topic, confirm feasibility, agree on a rough scope, and clarify next steps.

---

#### Step 1: Identify and Narrow Your Topic Idea

Before the meeting, formulate a clear — even if preliminary — topic idea. Avoid arriving with only a vague area of interest. Instead, try to answer these three questions in writing:

1. **What is the phenomenon or problem I want to study?** (e.g., *"Current object-detection models struggle with low-light environments in autonomous driving scenarios."*)
2. **Why does it matter?** (e.g., *"Night-time driving accounts for a disproportionate share of road accidents, yet most benchmarks focus on daytime conditions."*)
3. **What could a thesis contribute?** (e.g., *"A comparative evaluation of domain-adaptation techniques applied to low-light datasets."*)

Having at least a draft answer to all three will help you articulate your idea clearly and give Prof. Dr. Alvarez something concrete to react to.

---

#### Step 2: Review Relevant Prior Work

Spend 2–4 hours doing a preliminary literature search before the meeting. Use Google Scholar, IEEE Xplore, or ACM Digital Library. You do not need an exhaustive review — the goal is to:

- Confirm the topic is actively researched (showing it is relevant).
- Find 3–5 key papers so you can speak to the existing state of the art.
- Identify at least one clear gap or open question (this will become the seed of your research question).

Bring a short printed or digital list of the papers you found, noting the title, authors, year, and one sentence on why each is relevant.

---

#### Step 3: Draft a Preliminary Research Question

Based on your reading, try to write one research question before the meeting. A good research question is:

- **Specific** — not "How can AI be used in healthcare?" but "To what extent does fine-tuning a pre-trained vision transformer on a clinical skin-lesion dataset improve diagnostic accuracy compared to training from scratch?"
- **Feasible** — answerable with the resources and time available for a bachelor's or master's thesis.
- **Answerable** — it produces a concrete, verifiable answer, not just an opinion.

Bring your draft question to the meeting. It will almost certainly change, but having something concrete to discuss is far more productive than starting from zero in the room.

---

#### Step 4: Prepare Questions for the Professor

Come with a list of 4–6 questions. Examples:

- *"Is the scope I have in mind realistic for a [bachelor's / master's] thesis?"*
- *"Are there ongoing projects in your group that my thesis could build on or contribute to?"*
- *"What methodology would you recommend for this type of research question — empirical study, design science, systematic review?"*
- *"Are there specific datasets, tools, or industry partners I should be aware of?"*
- *"What does a strong exposé look like in your view — are there previous examples I could read?"*
- *"How often would we meet during the thesis, and what do you expect from check-ins?"*

---

#### Step 5: Prepare a One-Page Topic Summary (Optional but Recommended)

Writing a single page before the meeting forces you to think clearly and gives the professor a document to annotate. Structure it as follows:

```
Title (working):    [Your working thesis title]
Student:            [Your name], [Student ID]
Degree programme:   [BSc / MSc Computer Science]

Motivation (2–3 sentences):
  Why is this topic important right now?

Problem statement (2–3 sentences):
  What specific gap or deficiency does the thesis address?

Preliminary research question:
  RQ1: [Your draft research question]

Tentative approach (2–3 sentences):
  How do you plan to answer the question?

Key references (3–5 bullet points):
  - Author (Year). Title. Venue.
```

This one-pager maps almost directly onto the first two sections of the exposé template, so the work is never wasted.

---

#### Step 6: Logistics Checklist Before the Meeting

- [ ] Confirm the meeting date, time, and location (or video call link) with the professor's secretary or directly via email.
- [ ] Bring a notepad or open a notes document — you will want to record feedback, name suggestions, and action items.
- [ ] If remote: test your audio/video beforehand and share your one-pager in advance by email.
- [ ] After the meeting: send a brief follow-up email summarising the agreed-upon next steps and the (updated) research question. This keeps both parties aligned and creates a written record.

---

#### What to Expect in the Meeting

Prof. Dr. Alvarez will typically react to your idea by asking probing questions to test its feasibility and originality — this is normal and constructive, not a sign that the topic is bad. Common feedback themes include:

- The scope is too broad → narrow it to a specific system, dataset, or context.
- The research question is too descriptive → reframe it as an evaluative or comparative question.
- A very similar thesis was already written → discuss how to differentiate or build on it.
- The methodology is unclear → think more concretely about what data you will collect and how.

Treat the meeting as a collaborative brainstorming session, not a presentation to be judged. The goal is to leave with a clearer direction and concrete next steps — not a finished topic.

---

*Template maintained by Prof. Dr. Ignacio Alvarez · Faculty of Computer Science*
*Repository: [https://github.com/ignacioalvmar/thesis_expose_template](https://github.com/ignacioalvmar/thesis_expose_template)*
