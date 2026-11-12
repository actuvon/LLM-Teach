# README (usage notes)
> For Claude: copy this whole `_Template` folder to `./Evaluations/Evaluation N (Name)/` when generating a new evaluation, and link this `EvaluationPlan.md` from `Evaluations.md`. This file is also the doc `Kanban.md`'s "Active Tasks NOW" should link to while the evaluation is in progress — don't create a separate task stub. Fill in Scoring Criteria and Question Plan here FIRST, then write the actual questions into `EvaluationTemplate-A.md` (blank, fillable) and `AnswerKey-A.md` (questions + answers + grading notes) as a matched pair — every file in this folder carries its version letter in the name, `A` for the original, so the filename alone always tells you which version you're looking at. Keep **Status** current — this is the recovery point if a session ends or gets compacted mid-evaluation, same as a Lesson's Status field: `Not Started` → `Plan Drafted` → `Questions Written` → `Attempt N In Progress` (set the moment the user says they're beginning — before that point, avoid discussing this evaluation's content at all in case they're already reading it) → `Attempt N Submitted` → `Graded`. During the evaluation, don't teach, hint, or reveal the answer key — clarifying what a question asks is fine, guidance toward the answer is not. The user takes it by copying `EvaluationTemplate-A.md` to `Attempt-A1.md` (version letter + attempt number, starting at 1) in this folder, filling it out, and asking to be graded. Grade by comparing the attempt to the matching `AnswerKey-<letter>.md`, annotating each question directly in the attempt file (see its `**Grade:**` line), then rolling the overall score into the Attempts & Results table below, `Evaluations.md`, and `PredictedScores.md`. If the user asks to **scramble**, don't edit the originals — create a new `EvaluationTemplate-B.md` / `AnswerKey-B.md` pair (increment the letter for further scrambles) that tests the same Question Plan with different questions; attempts against a scrambled version follow the same pattern: `Attempt-B1.md`, `Attempt-B2.md`, etc. Add a row to the **Versions** table below the moment a version's question text is written (including Version A itself, at creation) — that table and the filenames should always agree on how many scramblings exist.
> For the human: no help is given here beyond clarification of what's being asked — that's what separates an evaluation from a lesson. To take this evaluation, copy `EvaluationTemplate-A.md` (or `EvaluationTemplate-B.md` etc. if scrambled) to `Attempt-A1.md` (matching that version's letter), fill it in, and ask to be graded.

# Evaluation N: (Name)

**Curriculum Items Covered:** (e.g. 3.1, 3.2)
**Format:** Quiz | Practical
**Date:**
**Status:** Not Started

## Scoring Criteria
(What counts as correct / partial / incorrect for each question or task, defined before writing questions.)

## Question Plan
(Themes/topics covered, how many questions per curriculum item, the mix of multiple choice / short answer / long answer / practical, and any shared context or scenario the questions should sit in. The actual question text and answers belong in each version's `EvaluationTemplate-<letter>.md` / `AnswerKey-<letter>.md`, not here — this section describes intent, not content, so it stays valid across scrambles.)

## Versions
| Version | Template | Answer Key | Status | Created |
| ------- | -------- | ---------- | ------ | ------- |
| A (original) | `EvaluationTemplate-A.md` | `AnswerKey-A.md` | Not Started | |

(Version A is always the original — add this row as soon as its question text is written, even before any attempt is taken. A scramble adds a new row, e.g. `B` → `EvaluationTemplate-B.md`/`AnswerKey-B.md`, when *its* question text is written. The filenames carry the same letter, so this table should never disagree with what's actually on disk.)

## Attempts & Results
| Attempt | Version | Date | Score | Notes |
| ------- | ------- | ---- | ----- | ----- |

(One row per `Attempt-A1.md`, `Attempt-B1.md` etc., added as each is graded.)
