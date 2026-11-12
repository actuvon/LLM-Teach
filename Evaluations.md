# README (usage notes)
> For Claude: generate an evaluation on request (or when a chunk of lessons is complete and warrants a check — including the placement diagnostic run before lessons are drafted, see `README.md`'s Learning Process). Copy `./Evaluations/_Template/` to `./Evaluations/Evaluation N (Name)/`. Fill in `EvaluationPlan.md` (scoring criteria, question plan) first, then write the matched pair `EvaluationTemplate-A.md` (fillable, no answers) and `AnswerKey-A.md` (questions + answers) — every file in an evaluation folder carries its version letter in the name (`A` for the original), so the filename alone tells you which version you're looking at; record it in `EvaluationPlan.md`'s Versions table too, the two should never disagree. Add a row here linking to `EvaluationPlan.md`. Keep `EvaluationPlan.md`'s **Status** field current through the lifecycle (`Not Started` → `Plan Drafted` → `Questions Written` → `Attempt N In Progress` → `Attempt N Submitted` → `Graded`) — it's the recovery point if a session ends mid-evaluation. The user takes it by copying `EvaluationTemplate-A.md` to `Attempt-A1.md` (version letter + attempt number) in that folder; grade it against `AnswerKey-A.md` (per-question feedback goes on each `**Grade:**` line in the attempt itself), then record the rollup score in `EvaluationPlan.md`'s Attempts & Results table and in the row/journal here. During an evaluation, do not teach, hint, or reveal the answer key — minor clarifying questions about what's being asked are fine, guidance toward the answer is not. If asked to **scramble**, generate a new `EvaluationTemplate-B.md` / `AnswerKey-B.md` pair (same plan, different questions) rather than editing the originals — attempts against it follow the same pattern, `Attempt-B1.md` etc. After scoring, update `PredictedScores.md` and log the reasoning there.
> For the human: evaluations are graded checkpoints, not lessons. Expect no help beyond clarifying what a question is asking. To take one, copy its `EvaluationTemplate-A.md` (or `-B`, `-C`... if scrambled) to `Attempt-A1.md` (matching that version's letter) and fill it in.

# Evaluations

| # | Date | Curriculum Items | Format | Score | Plan / Results |
| - | ---- | ----------------- | ------ | ----- | --------------- |

**Format values:** Quiz · Practical

## Evaluation Journal

| Date | Eval # | Notes / Observations |
| ---- | ------ | ---------------------- |
