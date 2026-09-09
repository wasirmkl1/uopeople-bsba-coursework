---
inclusion: always
---

# Rules for Writing UoPeople Assignments

This file records rules for writing and formatting UoPeople assignments, discussion posts,
and peer replies. Treat every rule below as a hard requirement, not a suggestion.

This file is intentionally generic (no student name baked into the rules themselves) so it
stays easy to maintain. Student-specific info — name, program, enrolled courses,
instructors, and schedule — lives in a separate `student-profile-*.md` file in this same
directory.

**This repository is independent from any other UoPeople coursework repository that may
exist for another student in the same household.** Do not reuse, reference, or copy
specific phrasing, examples, or content from another student's repository or assignments
into this one, even if the assignment topic happens to be the same (e.g., both students
have a UNIV 1002-01 course). Each student's writing must be their own, drafted from their
own answers and their own voice.

**How to use this file:** Sections 1, 2, 3, 5, 6, 7, 10, 11, 12, 13, and 14 apply to
*everything* — every written assignment, every discussion post, every peer reply, regardless
of course or unit. Sections 4, 8, and 9 apply only to the specific assignment *types* named
in their titles (SMART-goal assignments, discussion posts, and peer replies respectively) —
read the "Scope" line at the top of each of those sections before assuming a rule applies to
the task at hand.

**Start here for any new assignment or discussion (initial-post) request:** read Section 12
first — it governs *how* to begin drafting (ask before writing) before any of the other
rules about tone, formatting, or citations come into play. **Peer replies are the
exception** — see Section 9, item 7: skip the "ask before writing" step and generate the
reply immediately once the student provides the peer's post.

---

## 1. Citations and References — never fabricate, always verify
**Scope: universal — applies to every written assignment, discussion post, and peer reply.**

- **Never invent a source, a resource name, or a citation detail.** Before citing anything
  (a video, textbook, office, or service), verify it actually exists and get its real name,
  date, and URL. Do not claim a resource offers a service it doesn't (e.g., the UoPeople
  **Library and Resource Center (LRC)**, accessed via Library Services,
  library@uopeople.edu, has an Academic Writing module but does not offer live writing
  review/feedback appointments — do not describe it as if it does). When unsure what a
  service actually does, ask the student rather than guessing from search results.
- **Never fabricate a fact, statistic, or specific number to make a sentence sound more
  concrete.** If a number is not confirmed by the student or found in a real source, either
  omit it or say plainly that it is an estimate without an invented precision.
- **When paraphrasing a source's argument, verify the paraphrase against the source's
  actual wording, not just against the general topic.** A paraphrase that captures the
  general idea but changes a specific technical term can still be wrong — pull up the
  actual source text before finalizing any specific paraphrased claim, not just before
  finalizing a citation.
- **Every in-text citation must have exactly one matching reference-list entry, and every
  reference-list entry must be cited in-text at least once.** No orphans in either
  direction. Check this explicitly and programmatically (count occurrences of each citation
  form in the body text) before presenting any draft — do not eyeball it.
- **Confirm source relevance against the actual assigned reading/materials list** for that
  specific unit (the reading assignment page/HTML, or whatever the course provides), not
  from memory or general web search. Read the real assignment page before deciding what
  counts as "assigned" vs. "outside" source.
- **APA 7 reference formatting checklist** (check every one, every time, on every reference
  list):
  - Titles of standalone works (books, videos, reports) are *italicized*. Journal article
    titles are **not** italicized, but the *journal name* and *volume number* are.
  - **When citing one chapter from a regular (non-edited-volume) book, italicize the book
    title, not the chapter title.** Format: `Author, A. A. (Year). Chapter title. In *Book
    title: Subtitle*. Publisher. URL` — the chapter title stays in plain text; only the
    book title (including its subtitle) gets italicized.
  - **When more than one source is cited in the same parenthetical in-text citation, order
    them alphabetically by the same key used in the reference list** (first author's
    surname, or the organization/source name for group-authored sources like a YouTube
    channel), separated by semicolons — e.g., `(Author A, 2020; Author B, 2023)`, not the
    order the sources happen to be discussed in the sentence.
  - Author initials must have a **space between each initial** (e.g., "M. J." not "MJ.").
    This applies even if the original source material (e.g., a professor's own reading list)
    has it wrong — fix it in the student's own reference list regardless of the source's error.
  - **Group/organization authors** (a YouTube channel, a company, a nonprofit) are cited the
    same way as a person: `Organization Name. (Year, Month Day). *Title of video* [Video].
    YouTube. URL` — do not invent a personal author name for a source that is credited to an
    organization or channel.
  - Hanging indent (0.5") on every reference paragraph, double-spaced, no extra paragraph
    spacing.
  - **Every reference-list URL in a `.docx` must be a real, clickable hyperlink, not
    plain text that merely looks like a URL.** When generating the file (e.g., with
    `python-docx`), build each reference entry with an actual `w:hyperlink` element tied to
    a relationship in `word/_rels/document.xml.rels` (`python-docx` does not create this
    automatically from plain text — insert it explicitly via `part.relate_to(...)` and a
    manually constructed `w:hyperlink` run, or equivalent). **Do this as a required step,
    every time a `.docx` reference list is built — not only when the student asks about
    it or after a mistake is caught.** Before presenting any `.docx` as finished, verify
    programmatically that the number of hyperlink relationships in
    `word/_rels/document.xml.rels` matches the number of reference-list URLs (open the
    `.docx` as a zip and check `word/_rels/document.xml.rels` and the `<w:hyperlink>` count
    in `word/document.xml` — do not just eyeball the rendered text, since plain text and a
    real hyperlink can look identical in some viewers). Plain-text discussion posts (not
    submitted as `.docx`) should still include the full, correct URL as text, since there is
    no hyperlink mechanism to apply there.
  - **Treat the full APA 7 checklist above as mandatory for every `.docx` generated, every
    time** — re-run through italics, hanging indents, author-initial spacing, and the
    hyperlink check above as a standard pre-submission pass, not as something to apply only
    when a mistake has already been pointed out.
  - **Title page (APA 7, student paper format)** is expected for standalone written
    assignments submitted as a Word document unless the assignment's own instructions
    explicitly say otherwise — include one by default rather than waiting to be asked, with
    these elements centered and in this order, each on its own line, roughly in the
    vertical center of the page: paper title (bold), student's full name, university name,
    course number and full course name, instructor's name, and the date. Do not add a
    running head or "Author Note" section — those are APA 7 *professional*-paper elements,
    not required for a *student* paper.
  - **The title-page date is always the assignment's due date, never the actual date the
    student submits.** This holds even if the student finishes and submits early — the date
    on the cover page does not move to match the submission date. Confirmed against Purdue
    OWL's official APA 7 student-paper guidance.
  - **Timezone care when picking the due date:** the LMS may display a due date/time
    converted into the student's local timezone, while the underlying due date in the LMS's
    own reference timezone can be a different calendar date. Always use whichever calendar
    date the institution's system treats as the official due date, not a timezone-shifted
    display of it. If it's ever unclear which date is authoritative, ask the student to
    confirm via the course portal or the instructor rather than guessing.

## 2. Tone, Register, and AI-Pattern Avoidance — the single biggest point-loss risk
**Scope: universal.**

- **No established writing samples exist for this student yet.** Until real, previously
  submitted assignments from this student are available for this repository, default to a
  natural, first-person, moderately informal student voice rather than a stiff, formal,
  contraction-free academic register. Contractions ("doesn't," "isn't," "that's," "it's")
  are fine and often make writing sound more like a genuine student and less like an
  AI-generated essay — do not ban them outright.
- **As soon as the student has real submitted work in this repository** (in any course's
  `Assignments/` or `Discussions/` folder), read it before drafting anything new, and match
  that established voice going forward instead of the generic default above. Update this
  section with a note pointing to the specific sample files once that happens, the same way
  a parallel household repository for another student did after their first few
  assignments were available.
- Discussion posts follow the same natural-voice principle unless the specific course's own
  guidance says otherwise.
- **Never let a topic sentence just restate the assignment question**, and never let
  multiple paragraphs in the same piece open with the same grammatical construction (e.g.,
  several paragraphs in a row opening with a gerund: "Comparing...", "Looking...",
  "Applying..."). This reads as mechanical and AI-generated. Before presenting any draft,
  scan the first few words of every paragraph, and the first two words of every sentence, for
  repeated patterns — this must be checked explicitly (e.g., programmatically), not by
  skimming.
- **Do not claim something is true about the document that isn't** (e.g., writing "this
  source backs the argument" when the source only appears in a self-assessment, not the
  essay body). Read what a summary/self-assessment sentence is actually claiming and confirm
  it matches the document's real content before writing it.
- **When asked for sentence-structure variation or paraphrasing on a specific passage,
  re-verify the new version does not accidentally introduce a duplicate phrase elsewhere in
  the same document, or push the word count out of its required buffer** (see Section 3).
- **Aim for a natural, first-person student voice, not a stereotyped "beginner" voice.** Mix
  short and long sentences, vary paragraph and sentence openings, and switch between active
  and passive voice where it reads naturally rather than mechanically alternating them.
  Paraphrase instead of reusing the same phrasing across drafts or across assignments. As the
  term progresses, a real student's writing naturally grows more confident and fluent — do
  not force an artificially simplistic style just because it is an early unit.
- **Sanity-check any tool, technique, or concept referenced in a draft against the actual
  course level.** For an introductory course, avoid referencing tools, techniques, or
  concepts more advanced than what an intro-level student would plausibly know or that the
  course readings have actually covered, unless the student specifically asks for it. When
  unsure whether something is too advanced, ask.

## 3. Word Count Discipline
**Scope: universal — applies to every written assignment and discussion post with a stated
word range.**

- **Always leave a real buffer below the ceiling — 20–30 words minimum below the stated
  maximum**, not just "under the limit." Hitting the ceiling with only a few words to spare
  is fragile: a single later edit can push it over without warning.
- **Recompute the word count immediately after every single edit, including edits that look
  small.** Small edits accumulate, and a buffer that isn't actively re-checked after each
  change can silently disappear.
- Word count for most of these assignments excludes the title page and reference list —
  confirm this per-assignment from the actual instructions, don't assume it carries over
  from a previous unit.
- Discussion post word ranges are usually smaller and different from written-assignment
  ranges (e.g., 350–500 words for a discussion vs. 400–550 for an essay) — always recheck
  the specific range stated in that assignment's instructions rather than reusing a number
  from a different assignment type.
- **When building the final `.docx`, re-verify the word count from the actual saved file**,
  not just the plain-text draft that was reviewed — a title heading or bolded section
  header that exists in the `.docx` body but not in an earlier plain-text draft can shift
  the count by several words.

## 4. SMART Goals — what's actually graded
**Scope: narrow — applies only to assignments that specifically ask the student to write
S.M.A.R.T. goals (e.g., an Academic Success Plan or a goal-setting unit assignment). This
section has no bearing on general essays, most discussion posts, or peer replies — do not
apply "the five SMART elements" framework to unrelated writing.**

- The assignment rubric for this kind of task typically only checks that all five S.M.A.R.T.
  elements (Specific, Measurable, Achievable, Relevant, Time-bound) are **identifiable** in
  each goal. Goals are usually **not judged on whether the student actually achieves them
  later** — there is no follow-up or proof required unless the assignment says otherwise.
  Don't over-engineer goals for real-world accountability; focus on making each of the five
  elements clearly present and checkable in the text.
- Still use genuine, honest goals from the actual student — even though they aren't graded
  for real-world accuracy, an obviously fake or throwaway goal undermines the surrounding
  reflection paragraphs where the student describes their real relationship to goal-setting.
- When a goal requires a date, place it **comfortably inside** the stated window (e.g., if
  the assignment says "5–6 months," pick something landing around month 5, not exactly at
  the 5- or 6-month boundary), so that different starting-point assumptions (today's date vs.
  the assignment's due date) don't accidentally push it outside the range.

## 5. Verification Process — do this before ever presenting a draft
**Scope: universal — this is the checklist to run on every piece of writing before calling
it "final" or "ready," regardless of type.**

1. Word count (body only, per that specific assignment's stated exclusions).
2. All required vocabulary words (if any) present and used naturally in context.
3. Every citation has exactly one matching reference and vice versa.
4. Font, size, spacing match the assignment's stated formatting requirements, and — for
   every `.docx` file specifically — full APA 7 formatting per the Section 1 checklist,
   including that every reference-list URL is a real clickable hyperlink (verified via the
   `.docx` zip's `word/_rels/document.xml.rels` and `<w:hyperlink>` count, not by eye).
5. No leftover fabricated resource names, unverified facts, or duplicated phrases — scan
   for repeated word sequences (n-grams) after any edit, not just once at the very end.
6. Read the entire document fresh, not just the diff, since an edit made to fix one problem
   can have side effects elsewhere in the text that a narrow re-read would miss.
7. For discussion posts and peer replies specifically: also run the cross-document checks in
   Section 11 before presenting.

## 6. AI-Detection and Third-Party "Reviews"
**Scope: universal.**

- No one — not this assistant, not the student, not Turnitin itself — can reliably predict
  what an AI-detection tool will output. Treat any "GPTZero would probably say X%" or
  "ZeroGPT might flag this" statement as speculation, not evidence. Turnitin's own
  documentation states its AI indicator should not be used alone to judge a paper.
- **When another AI assistant, or any second review pass, makes a specific factual claim
  about a document (a vocabulary count, a word count, "9 words used," etc.), verify it
  against the actual saved file before trusting or repeating it.** Never propagate an
  unverified claim from any outside source, including other AI outputs, without checking
  it first.

## 7. Workflow / Repo Practices
**Scope: universal for anything involving git/file operations.**

- Always push completed assignment work to a **new branch and open a pull request** —
  never commit directly to `main`, unless the student explicitly asks for a direct push to
  main for finished, verified work.
- After any fix, re-verify the *entire* document from scratch (see Section 5) — don't assume
  a targeted edit only affected the part that was changed.
- **Filesystem sync lag between tools can cause a script to load a stale or incomplete copy
  of a file and silently overwrite good content with it.** After any bulk-edit script,
  immediately re-read the saved file back and confirm all expected sections/content are
  still present before proceeding or reporting success.
- **Only initial discussion posts get saved into this repo's `Discussions/` folders.**
  Peer replies are drafted for the student to post directly to the course platform, but are
  not saved as files in the repo unless the student explicitly asks to keep a copy. Do not
  add a peer-reply file to `Discussions/` by default after drafting one.
- Attached files (PDFs especially, and previous-assignment `.docx` files uploaded through
  the GitHub web UI) can take time to sync into the workspace after the student says they've
  uploaded them. If a file isn't found immediately, re-check with a fresh directory listing
  or a fresh git pull before telling the student it's missing — don't assume it doesn't
  exist just because the first check came back empty. **Important:** files uploaded this way
  can land as a new commit directly on `main` (bypassing any local branch this assistant
  happens to be on), so if a file still can't be found after checking the current branch,
  check out `main` and pull before concluding it is missing.
- Some PDFs are scanned/image-based with no extractable text layer (a plain text-extraction
  tool will silently return an empty string, which can look like "no content" rather than
  "wrong extraction method"). If text extraction returns 0 characters, check for `/XObject`
  resources on the page (a sign of embedded images) and fall back to rendering each page to
  an image (e.g., via PyMuPDF/fitz `get_pixmap()`) and reading the images directly.

## 8. Discussion Forum Posts
**Scope: narrow — applies specifically to discussion-board-style assignments (an initial
post plus peer replies), as distinct from standalone written assignments/essays.**

- Discussion posts have their own rubric, separate from written assignments, typically
  scored on: identifying specific behaviors with resource support, explaining
  prioritization/methods clearly, explaining *why* those methods improve outcomes, connection
  to course materials (with citations), clarity and mechanics, timeliness of the initial post
  (usually due before peer replies), word count, and peer reply quality. Always read the
  actual rubric criteria for that specific assignment rather than assuming a generic
  structure will satisfy it — the exact point breakdown varies by unit.
- If the assignment references a specific in-textbook exercise or table, locate the actual
  textbook section and pull any real numbers it provides rather than inventing
  precise-sounding numbers the student never measured. See Section 1's fabrication rule. If
  a specific number is not strictly required by the rubric, prefer omitting it over guessing.
- Do not assume more citations are automatically better. Check the actual rubric wording
  (e.g., "at least one assigned resource") before adding sources — padding a discussion post
  with unnecessary citations can look formulaic and rarely raises the score once the minimum
  is already met with sources that are doing real argumentative work. See Section 10 for the
  standing three-question reference check to run on every draft.
- **Platform mechanic — the student must post before she can view or reply to anyone.** On
  this course platform, the student's own initial discussion post must be submitted before
  classmates' posts become visible to her at all, and she can only reply after that. This is
  a platform restriction, not a personal preference — never suggest drafting a peer reply
  before the student's own initial post for that unit has already been submitted, and don't
  assume classmate posts are viewable/available until she confirms she's posted hers.

## 9. Peer Reply System (Discussion Forums)
**Scope: narrow — applies specifically to peer replies within a discussion forum
assignment, not to initial posts (see Section 8 for those) or standalone assignments.**

UoPeople discussion assignments typically require replying to at least two classmates'
posts by a set deadline (e.g., Wednesday, following an initial-post deadline like Sunday).
Follow this process every time:

1. **Read the actual "Guidelines for Meaningful Peer Replies" document for the specific
   course**, if the student has provided or referenced one — it may be an image-based PDF
   (see Section 7 for how to read those). Do not assume a generic reply structure without
   checking it first, since guidelines can vary by course.
2. **Pick posts worth replying to based on substance, not convenience.** A good reply target
   introduces a genuinely different angle, behavior, or framework than the student's own
   post, or than a peer's earlier reply. Assignment rubrics often also ask students to
   prefer posts with fewer existing replies, so classmates get a fair chance to be responded
   to.
3. **Structure each reply around this template**: acknowledge a specific point from the
   peer's post → connect it to the replier's own experience or a genuinely different angle
   (not just restating agreement) → ask one or two open-ended, non-rhetorical questions that
   invite a real follow-up → close briefly and supportively. Do not evaluate or grade the
   peer's work — peer replies are collaborative, not corrective.
4. **Verify every specific claim made about the peer's post against their actual text**
   before finalizing a reply. Do not paraphrase loosely if the peer used specific wording —
   match their actual phrases so the reply reads as genuinely responsive rather than a
   generic gloss.
5. **Keep peer replies concise: roughly 3–4 sentences.** A peer reply is a quick, focused
   conversational contribution, not a second essay. See item 8 below for the hard word cap.
6. **Do not ask the student whether other classmates have already replied to a given post.**
   When the student hands over a classmate's post to reply to, she will include the full
   thread — the peer's post plus any existing replies to it — in what she gives you, if any
   exist. Use whatever thread content she provides as-is; if she doesn't include any existing
   replies, treat that as meaning there are none, and do not stop to ask.
7. **Skip the Section 12 "ask before writing" step for peer replies specifically.** The
   student has already supplied the peer's post (and any existing replies) and the
   "Guidelines for Meaningful Peer Replies" resource is already available — generate the
   full reply immediately in one pass, in the student's voice, without pausing for
   direction, feedback, or approach confirmation first. Still show the complete reply text
   for her to review/copy before it gets posted to the platform.
8. **Keep every peer reply under 150 words — this is the single hard cap, not 130.** If a
   first draft runs long, trim rather than pad — prefer cutting the acknowledgment or
   closing line before cutting either question, since the question is what invites a
   genuine follow-up.
9. Apply the same tone rules as Section 2 (natural student voice, contractions allowed)
   unless the specific course's guidelines say otherwise.

## 10. "Do I need more references?" — a standing question to answer, not assume
**Scope: universal for any piece of writing that includes citations.**

Whenever a draft is presented for review, proactively answer these three questions about
its sources — don't wait to be asked:

1. **Does every reference-list entry have a matching in-text citation, and does every
   in-text citation have a matching reference-list entry?** Check this programmatically
   (count occurrences of each citation form in the body text), not by eye. Report the result
   explicitly (e.g., "confirmed: X citations, Y references, no orphans either direction")
   rather than a vague "looks fine."
2. **Is each source actually relevant to the assignment**, verified against the real
   assigned materials list (not memory or assumption)? A citation that is technically present
   but doing no real argumentative work is padding, not evidence.
3. **Are more references actually needed?** Check the specific rubric wording rather than
   assuming "more is always better." If the current sources already satisfy the stated
   minimum and are each doing real work, say so directly and recommend against padding.

This same "answer proactively, don't wait to be asked" habit should extend to every item in
the Section 5 verification checklist — state the word count, the citation match, and the
formatting check results directly when presenting a draft, rather than only producing them
when the student separately asks.

## 11. Cross-Document AI-Pattern and Overlap Checks
**Scope: universal whenever more than one piece of writing exists in the same session or
the same course thread** — this includes two peer replies, or an essay and a discussion
post.

- **Check for identical or near-identical sentence structures used to open the same
  *position* in different pieces** (e.g., the same opening phrase repeated across different
  assignments' closing paragraphs, or the same phrase repeated across two different peer
  replies). This will not be caught by checking each document in isolation, since each
  individual document can look fine on its own while still forming a recognizable pattern
  across the set — the comparison must be done deliberately and explicitly.
- **Do not reuse specific phrasing, examples, or content from a different student's
  coursework repository, even if that other repository covers the same assignment topic in
  the same or a different course section.** Each student's writing must read as their own
  independent account, drafted from their own answers.
- The same overlap check applies to a discussion post against the specific classmates' posts
  it is going to reply to, or that were already replied to in the same thread — don't reuse
  a peer's specific wording as if it were the replier's own observation.

## 12. Collaborative Drafting Process — ask before writing personal content
**Scope: universal — read this before starting to draft any new assignment, discussion
post, or peer reply.**

- **Do not write personal-reflection, opinion-based, or experience-based content
  unilaterally.** When an assignment or discussion asks for the student's own experience,
  opinion, goals, or reflection, ask targeted questions first and draft using the student's
  actual answers, adapted into polished prose — do not invent generic filler reflection on
  the student's behalf and present it as if it were their own account.
- **For purely technical or conceptual content** where no personal experience is required,
  drafting directly is fine. Even then, if the assignment allows more than one reasonable
  approach (e.g., a choice of scenario, example, or structure), briefly confirm the approach
  with the student before writing a full draft rather than assuming silently.
- Ask questions **meaningfully and batched at the start** of a new drafting task — do not
  turn a request into a long back-and-forth of trivial micro-questions. A short, well-chosen
  set of questions upfront is enough; use the answers to write a complete first draft.
- When it is genuinely unclear whether a given part of an assignment needs the student's
  personal input versus being purely technical, ask rather than guess.

## 13. Presentation and Review Discipline
**Scope: universal — governs how drafts are shown and when work gets pushed to git.**

- **Always show the complete document when presenting a draft or a revision for review** —
  the full text, including the full reference list — never only a diff or a snippet. The
  student needs to see the whole thing every time to review it properly.
- **Never push or commit finished work to git automatically.** Present the finished draft
  (or the built file, e.g., a `.docx`) to the student first and wait for their explicit
  approval ("looks good," "go ahead," etc.) before creating a branch, committing, pushing,
  or opening a pull request. This applies even if a draft appears fully correct.
- **When asked whether a piece of writing "sounds like a student" or "would detect as AI,"
  give an honest, specific critique of the actual text** — point to concrete tells such as
  repeated paragraph or sentence openings, uniform sentence length or structure, overly
  formal or generic transitions, or a lack of personal voice — rather than deflecting
  entirely. The deflection in Section 6 ("no one can predict a detector's numeric score")
  applies only to guessing what a specific AI-detection tool would output; it does not excuse
  skipping a genuine, specific read of whether the prose itself sounds natural.

## 14. Vocabulary Highlighting
**Scope: universal.**

- **Only bold or otherwise highlight vocabulary terms in an assignment when that specific
  assignment's own instructions explicitly require using vocabulary words from a provided
  list.** Do not proactively highlight vocabulary in a draft by default. Always check the
  actual assignment instructions for a stated vocabulary requirement before deciding whether
  to highlight anything — do not carry a highlighting habit over from one course or unit to
  another without checking.

## 15. Document Metadata — no generator fingerprints in the final `.docx`
**Scope: universal for every `.docx` file built and submitted from this repo.**

- **Tools used to generate a `.docx` (e.g., `python-docx`) leave identifying fingerprints in
  the file's hidden metadata by default**, even when the visible document text looks
  completely normal. A default `python-docx` save stamps `docProps/core.xml` with
  `<dc:creator>python-docx</dc:creator>` and `<dc:description>generated by
  python-docx</dc:description>`, and leaves `docProps/app.xml` statistics (`<Words>`,
  `<Characters>`, `<Paragraphs>`, `<Lines>`, `<Pages>`, `<TotalTime>`) all at `0`, which does
  not match a file that was actually typed and saved in Word. Anyone who checks File >
  Properties, or inspects the raw XML inside the `.docx` zip archive, would see this
  immediately.
- **Before considering any generated `.docx` final, explicitly set and verify these fields**:
  - `docProps/core.xml`: `creator` and `lastModifiedBy` must be set to the student's real
    full name (from the relevant `student-profile-*.md`), never left as a tool's default.
    `description`, `keywords`, and `category` should be empty, not a tool-generated string.
  - `docProps/app.xml`: `Words`, `Characters`, `CharactersWithSpaces`, `Lines`, `Paragraphs`,
    and `Pages` should hold plausible non-zero values consistent with the document's actual
    length (roughly matching the real word/paragraph counts already computed for the word
    count check in Section 3) rather than being left at the generator's default of `0`.
    `TotalTime` should be a plausible small nonzero number of minutes, not `0`.
  - Scan every file inside the `.docx` zip package (not just the visible document text) for
    any literal occurrence of `python-docx`, `python_docx`, or similar generator-tool
    signatures, and confirm none are present.
  - `python-docx` does not expose setters for the `app.xml` statistics fields directly;
    editing that XML part inside the zip archive after saving is the correct way to fix it
    (verify the round trip still opens correctly afterward).
- **Do this check as a required step before presenting any `.docx` as finished**, the same
  way word count and citation matching are checked in Section 5 — not only when the student
  specifically asks about it.


## 16. Exam Question Banks
**Scope: universal — reference this whenever the student asks exam/quiz multiple-choice or
true-false questions to be answered.**

- **BUS 1101-01 exam Q&A is tracked in a running question bank file, not answered from
  scratch each session.** Location:
  `Term_01/BUS 1101-01 Principles of Business Management - AY2026-T5/Exams/Question_Bank.md`.
  Before answering a new batch of questions for this course, check this file first — the
  student may be re-asking a question that's already been verified, or may want a new batch
  appended in the same "Set N" format already used there.
- When the student provides a new batch of exam questions, verify each answer against
  reliable sources (course materials if available, otherwise reputable business/management
  references), then append a new numbered "Set" to the same file rather than creating a
  new file per exam. Keep the same format: full question text, all answer options, then a
  bolded `**Answer:**` line, with a brief explanatory note for any non-obvious or
  frequently-confused answer.
- If other courses accumulate their own exam question banks later, follow the same pattern:
  one `Question_Bank.md` inside that course's own `Exams/` folder.
