---
inclusion: always
---

# Quiz Answer Bank Workflow

When the user sends quiz/exam questions to be answered for any course in this repo, follow
this process. (This mirrors the workflow used in the household's other UoPeople repo, but
per this repo's own cross-student policy above, no actual question/answer content is shared
or copied between repos — only the process below.)

## Where the answer bank lives

Each course gets its own verified answer bank at:

`Term_N/<Course folder name>/Exams/uopeople-verified-quiz-answers.md`

Create this file the first time quiz questions come in for a course that doesn't have one
yet, using the structure described below.

Existing answer banks in this repo:

- **ENGL 1102-01:** `Term_02/ENGL 1102-01 English Composition 2 - AY2027-T1/Exams/uopeople-verified-quiz-answers.md`
  (Unit 1 finished. Note: this specific file's content was explicitly requested to be
  copied into this repo from the household's other UoPeople repo, as a one-off exception to
  the no-cross-referencing policy above — the user made that call directly. Don't treat this
  as a standing precedent for copying other content between the two repos without a similarly
  explicit request.)

## Answering process — sourcing order for every new question

1. **That course's own `uopeople-verified-quiz-answers.md` file**, if one already exists —
   check for an exact or near-exact match (same question, same or reordered options) before
   doing anything else.
2. **The course's actual assigned Readings** (unit reading HTML pages, textbook
   chapters/sections named in them, video transcripts) — read the real material directly,
   don't answer from general recollection of the subject.
3. **The open internet**, only if steps 1–2 don't resolve it — and say explicitly when an
   answer relies on this step rather than the course's own materials. Course-specific quiz
   keys can diverge from the strict/standard textbook definition of a concept; when that
   happens, note it as a trap for that specific question rather than silently overriding it.

## Logging rule — confirm before logging, every time, no exceptions

**Do not write a new answer into any `uopeople-verified-quiz-answers.md` file until the user
has explicitly confirmed the real result of that specific question** (told you it scored
correct or incorrect on an actual quiz/self-quiz attempt). Do not log answers that are only
the assistant's own reasoning and haven't been confirmed yet — present them in chat first,
wait for the user's confirmation of the batch, and only then write them to the file.

When the user does confirm a batch, log each item with the right label:
- **CONFIRMED CORRECT** — user confirmed this scored correct.
- **CONFIRMED WRONG** — user confirmed this scored incorrect (note what the actual correct
  answer turned out to be, if known, so the trap is documented for next time).
- **REASONED (unconfirmed)** — only used if explicitly asked to log a not-yet-graded guess
  for future reference; never the default.

If a previously logged CONFIRMED entry is later contradicted by a new result (e.g., the
option set changes, or the same question is later confirmed with the opposite answer),
correct that entry in place and note both the old and new answer so the trap stays visible,
rather than leaving the outdated line standing unexplained.

## Repo push behavior for this file type

Unless the user says otherwise, commit and push updates to these answer-bank files directly
to `main` (this differs from the assignment/discussion branch-and-PR workflow in Section 7
of `assignment-writing-rules.md`, since answer banks are reference notes rather than graded
submissions) — but only once the user has said it's fine to push, and only after the
confirm-before-log rule above has already been followed for the content being pushed.
