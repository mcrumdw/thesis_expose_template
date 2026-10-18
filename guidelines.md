# Exposé Guidelines — Makram, B.Sc. UX Design (THI), supervisor Prof. Alvarez

This file adapts the default THI exposé guidance to Prof. Alvarez's own notes for students.
It is the workspace override that the thesis-proposal skills (write, check, review, publish) read.
Put it in the root of the exposé repo, next to the proposal file.

## The one rule: this is a project plan, not a mini-thesis

The exposé exists so the supervisor can approve a plan and the thesis can be registered.
It has to show three things: the problem is real, the question is answerable, and the study fits the time.
Everything that doesn't serve one of those three gets cut.

- Bachelor level means **applying existing knowledge to a well-defined problem**. The student carries about 60% of the project responsibility. The exposé does not need to prove novelty at master's depth.
- Target 6–8 pages of body text, using the template's per-section lengths as the ceiling, not the floor.
- One idea per paragraph. If a paragraph needs three citations to stand, it is probably doing literature review inside the introduction.
- No preliminary chapter outline, no code, no deliverables, no personal data in the body. Supervisor and student details go on the title page only.

## Structure (from the template — keep it, don't decorate it)

| # | Section | Length | What it must answer |
|---|---|---|---|
| 1 | Introduction and Motivation | 1–2 p | Why does this matter now, and what is out of scope? Write it last. |
| 2 | Problem Statement and Research Questions | 0.5–1 p | What exactly is missing, and what will the thesis find out? |
| 3 | Objectives | 0.5 p | What will the work *do* (action verbs)? |
| 4 | Related Work | 1–2 p | What is known, what's the gap, which theory frames it? |
| 5 | Methodology: Controlled Experiment | 1–2 p | How is each RQ answered, with which variables and how many participants? |
| 6 | Expected Contributions and Results | 0.5–1 p | What remains for others afterwards, and what are the limits? |
| 7 | Work Plan and Schedule | 1 p | Gantt chart at week granularity, with buffer. |

Methodology branch: **Controlled Experiment** (within-subject: LLM assistant vs. human Wizard-of-Oz co-driver, driving simulator).
Required subsections: Use Case Definition, Independent Variables, Dependent Variables, Procedure, Statistical Analysis.
Ethics goes inside Procedure, not in a separate section.

## Prof. Alvarez's requirements, mapped to sections

### Problem and framing (sections 2 and 4)

- **Research gap grounded in peer-reviewed literature.** The gap must be a limitation of current knowledge stated in a source, not an opinion. Name the gap in one sentence at the end of Related Work and point to the RQs.
- **SMART research questions.** Each RQ is Specific, Measurable, Achievable, Relevant, and Time-bound.
  - Measurable means every RQ maps to at least one dependent variable in section 5.
  - Achievable means answerable with one within-subject study in the THI simulator.
  - Time-bound is carried by the work plan; the RQ itself doesn't need a date.
- One to three RQs. Analytical wording ("to what extent", "how does … differ"), never yes/no, never "how can X be built".
- **Theoretical framework ("lens").** Name one theory that links the problem to how the data will be interpreted, and say in two or three sentences how it shapes the dependent variables.
  Candidates worth considering for this topic: Multiple Resource Theory (Wickens) for voice interaction under driving load, or the Technology Acceptance Model / trust-in-automation models (Lee & See) for user perception of the assistant.
  Pick one. A framework that is named but never used in the methodology doesn't count.

### Literature (section 4)

- **Synthesize, don't summarize.** Group sources into 2–3 thematic clusters, e.g.
  1. in-car voice assistants and driver distraction,
  2. LLM-based conversational agents and Wizard-of-Oz as a benchmark,
  3. language/culture effects in in-vehicle interaction (German-speaking drivers).
  Each cluster ends with what its studies share as a limitation. No paper-by-paper walkthrough.
- **Reference count: maximum 10 papers.** This overrides the skills' default working range of 10–15. With the check's floor of 10, the reference list holds exactly 10 entries. Every one must be cited in the text and earn its place under the five jobs below. When a new source comes in, an existing one goes out.

#### Trimming the reference list (current draft has ~22 → cut to 10)

Keep a source only if it does at least one of these jobs.
A rough budget for the 10 slots: 1–2 problem, 3–4 variables/instruments, 2–3 direct neighbours, 1 lens, 1 method.

1. **Proves the problem exists** (introduction) — one or two sources, the strongest ones.
2. **Defines or measures a variable** you actually use (e.g. the NASA-TLX paper if you measure workload, the SUS paper if you measure usability).
3. **Is a direct neighbour** — closest prior study you compare against or build on (e.g. the PromptDrive Germany–Mexico paper).
4. **Supplies the theoretical lens.**
5. **Justifies a method choice** (Wizard-of-Oz, within-subject design, the simulator).

Cut if: it's cited once to support a generic claim another source already covers; it's a vendor page or blog; it's a preprint when a peer-reviewed version exists; it's background you'd only need in the thesis itself.
Moved-out sources are not lost: park them in the Miro "Papers" section for the thesis.

### Variables and confounds (section 5)

- **Operationalize every concept.** Each abstract concept becomes a named measure with instrument and unit. Write it as a table:

  | Concept | Measure | Instrument / unit | RQ |
  |---|---|---|---|
  | e.g. Workload | Perceived workload | NASA-TLX, 0–100 | RQ1 |
  | e.g. Driving safety | Lane-keeping | SDLP in m, from simulator log | RQ1 |
  | e.g. Interaction quality | … | … | RQ2 |

  The table is the example of the format; fill it with what the study actually measures.
- **Independent variable**: assistant type, 2 levels (LLM vs. human WoZ). Add language (German/English) only if it is really manipulated; otherwise it is a sample characteristic or a control.
- **Address confounding factors** explicitly. The ones this design invites, and the usual control:
  - order and learning effects → counterbalance condition order (AB/BA), randomly assigned;
  - wizard behaviour drift → scripted wizard guidelines, same voice output (TTS) for both conditions so participants can't tell by voice;
  - response latency difference → match or log latency and report it;
  - route/task difficulty → matched scenarios, scenario order counterbalanced independently of condition;
  - language proficiency and prior voice-assistant use → screen and record as covariates;
  - simulator sickness → screening questionnaire, exclusion rule stated in advance.
- **Hypotheses**: state the falsifiable hypotheses in the opening paragraph of section 5, one per RQ.

### Rigor and ethics (section 5)

- **Justify sample size with a power analysis**, not availability. State α, power, and expected effect size, and where the effect size comes from (prior study or a conservative assumption).
  Example of the expected sentence: "An a-priori power analysis (G*Power; paired t-test, two-tailed, α = .05, power = .80, d_z = 0.5) yields N = 34."
  If the realistic recruitment is lower, say so and state which effect size the study can still detect.
- **Reproducibility**: state randomization (who gets which order and how), blinding (are participants told one condition is human?), and inclusion/exclusion criteria (driving licence, German proficiency level, age range, no simulator-sickness history).
- **Ethics, in two or three sentences inside Procedure**:
  - informed consent: what participants are told, when, how it's recorded — including the Wizard-of-Oz deception and the debriefing afterwards;
  - risk: simulator sickness, how participants can stop at any time;
  - data: what's recorded (audio, video, driving logs), pseudonymization, retention period, GDPR basis;
  - the ethics route / approval needed at THI before data collection.

### Work plan (section 7)

- Week-granularity table, one row per task, explicit start and end weeks (it becomes the Gantt chart).
- Milestones: registration, ethics approval, pilot study, data collection done, mid-point check-in, submission.
- Pilot before main study. Buffer of at least two weeks before submission.
- Three to five sentences naming the critical path (e.g. ethics approval → recruitment → data collection).

## Format (Prof. Alvarez's notes; the template already handles most of this)

- Use the LaTeX template unchanged — "formatting deviations often suggest a lack of attention to detail."
- Body font: Times New Roman 10–12 pt, or Arial/Helvetica. Line spacing 1.5. Inner margin 1.5 in for binding.
- Accessibility: linked table of contents and tagged headings (keep `hyperref`; don't fake headings with bold text).
- Citations: BibTeX, `dinat` style, DOI on every entry that has one. Keys like `Smith26Deep`.
- Remove every teal `\guidance{…}` block before sending.

## Writing style

- English, third person ("the thesis", "the study"), active voice, short sentences.
- Define abbreviations at first use: Large Language Model (LLM), Wizard-of-Oz (WoZ), Human-Machine Interface (HMI).
- Expectations are stated as expectations ("it is expected that"), never as results.
- No marketing language, no repetition across sections.

## Hand-in checklist

- [ ] 1–3 SMART RQs, each mapped to at least one dependent variable
- [ ] One named theoretical lens, used in section 5
- [ ] Gap stated in one sentence, grounded in a peer-reviewed source
- [ ] Operationalization table complete
- [ ] Confounds listed with their control
- [ ] Power analysis with α, power, effect size and its source
- [ ] Randomization, blinding, inclusion/exclusion stated
- [ ] Consent, risk, data handling covered in Procedure
- [ ] Exactly 10 references (max 10), all peer-reviewed or standards, all cited in text
- [ ] Gantt chart with pilot, ethics approval and buffer
- [ ] No `\guidance` blocks, no TODOs, compiles cleanly
- [ ] Emailed as PDF to Prof. Alvarez, then book open-hours slot

```toml
min_references = 10
```
