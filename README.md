# LLM-Teach

A blank template for an AI-driven learning experience: Claude acts as teacher, this repo's markdown files act as its state and memory, and you (the student) work through a curriculum built collaboratively with it.

## Getting Started

1. Fill in the **Learning Objective** below — as specific or as loose as you want it. One sentence is enough to start.
2. Open a Claude Code session in this repo.
3. Tell Claude to read `CLAUDE.md` and this file, then start bootstrapping: drafting `Curriculum.md`, running a placement diagnostic, and planning the first lesson. See **Learning Process** below for the full sequence.

## Learning Objective

**(fill this in — what do you want to learn, and how deep/how long do you want to go?)**

# Repo Structure

| Path                                    | Description                                                                                                                                       |
| --------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| ./Curriculum.md                         | The top-level curriculum that we are working through as we learn.                                                                                 |
| ./Lessons.md                            | Lists the different lessons we will go through to teach a part of the curriculum.                                                                 |
| ./Lessons/                              | This directory hosts the individual folders for each lesson.                                                                                      |
| ./Lessons/Lesson 1 (NAME)/LessonPlan.md | Each lesson has a lesson plan that describes the outline of the lesson, what the user is to do, what curriculum items are to be covered, how long |
| ./ActiveTasks/                          | Stores the status of the learning program, contains a Kanban board to facilitate using CLAUDE as a state machine.                                 |
| ./ActiveTasks/Kanban.md                 | The master list of what we are doing now, and what is on the TODO list.                                                                           |
| ./PredictedScores.md                    | A table of each curriculum item and an estimation (0-100%) of how well the user understands it, plus a change journal.                            |
| ./Evaluations.md                        | A table of formal evaluations (quizzes or practical tests with scoring criteria) listing the evaluation number, criteria covered, and score.      |
| ./Evaluations/                          | Stores evaluation plans and evaluation results similarly to how Lessons are stored.                                                               |
| ./Lessons/_Template/                    | Copy-and-fill starting point for a new lesson folder.                                                                                              |
| ./Evaluations/_Template/                | Copy-and-fill starting point for a new evaluation folder.                                                                                          |
| ./ActiveTasks/Archive/                  | Completed task detail files, moved here once done and folded into active docs.                                                                    |

# Architecture

## Curriculum
We start with the `Curriculum.md`. This is the map of knowledge we want to cover. Things are itemized so we can track what we have covered and what is left, and reference things cleanly.

## Learning Process
The course of a learning repository involves the following:
  - Identify the learning objective
  - Draft a curriculum
  - Perform a quick diagnostic/placement evaluation to establish the user's existing level of knowledge
  - Rework the curriculum to the user's needs, based on the diagnostic evaluation, so as not to spend too much time on what is already known
  - Draft the lesson plans
  - Complete lessons
  - Continuously estimate predicted scores
  - Evaluate the user's knowledge of the curriculum
  - Repeat adding and/or repeating lessons and/or evaluations until the user's score in all categories is to their satisfaction.

## Lessons
Lessons are all designed to take a certain amount of time so that the summed time of all lessons adds up to the desired amount of time and learning depth outlined.
A lesson will cover one or more item in the `Curriculum.md` and is 'chunked' based on a sort of functional task scenario that the AI guides the user through,
so the user has to use a simple set of tools to help them learn the objective subset of items from the curriculum by the end of the lesson.

Lessons are numbered and briefly described in `Lessons.md`. The description includes how long the lesson should take, what will be done, and what curriculum items will be covered,
but only VERY BRIEFLY. The detailed lesson plans go in the LessonPlan.md file in each `./Lessons/Lesson X YYYY/` folder.

If multiple claude sessions are needed for a single lesson to maintain working memory policy, advise the user when to shut down a session and spin up a new one, and update the docs appropriately.

Any and all files generated during a lesson go in the folder for that lesson.
The ActiveTasks folder helps us keep track of our status in lessons, particularly if they run multiple sessions.

## Predicted Scores
We we go through lessons and do evaluations and otherwise interact with the AI, our predicted scores are updated, giving a running indication of our perceived understanding of each item in the curriculum.
`PredictedScores.md` has a table of each curriculum item and an estimate from 0% understanding to 100% understanding that predicts how well the user has understood each item compared to
the Learning Objective.

A change journal table is kept at the bottom, and must be updated whenever making a change. This helps us see our progress over time.

## Evaluations
Evaluations can be generated on request to examine the user's understanding of one or more curriculum items. An evaluation is similar to a Lesson but no guidance is given, except maybe minor questions
to clarify the intent of a question, but certainly not to give away answers.
`Evaluations.md` keeps a table of all the numbered evaluations generated, what they cover, and what the user scored last. An Evaluation Journal is kept at the bottom of the document to track updates over time.

When generating an evaluation, copy the evaluation template as per the README instructions on evaluations. Three documents are made:
  - `The evaluation plan:` outlines the evaluation curriculum, criteria, scoring rules, context, number and theme of each type of question, etc...
  - `The fillable evaluation template:` is the 'test' that the user fills out. It outlines the questions, and provides a space for the user to answer them. Each test has a selection of multiple choice questions, short answer questions, and possibly long-answer, or other styles of questions, at the discretion of the teacher and the guidance of the prompt given to create the evaluation.
  When the user is doing the evaluation, he copies the template to a new file, marking the attempt number, fills out the evaluation, then asks the teacher to grade it.
  - `The answer key:` contains all the questions and answers. When grading the evaluation, the filled evaluation is compared against the answer key.

Evaluations are structured in such a way that it is possible for them to be taken more than once, although the user may ask for the evaluation to be **scrambled**. Scrambling an evaluation means making a new, separate fillable evaluation template and answer key, following the same evaluation plan, but using different questions to accomplish the same evaluation objectives.

When the user is doing an evaluation, the typical process goes as follows...
  - The user asks the teacher to generate a new evaluation or scramble a new fillable template, and the AI does so, preparing the new fillable evaluation.
  - The user indicates that they are beginning the evaluation and leaves the claude session open. Claude can respond to clarification questions about the evaluation but will not give away answers to questions.
  - Meanwhile, the user fills out the evaluation.
  - The user indicates to the claude session that they are done filling the evaluation, and asks for it to be graded.
  - The claude session grades the evaluation, asking clarifying questions to the student if necessary.
  - The claude session informs the user of their result, and updates the repo documents to track the history.
