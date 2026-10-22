# One Hundred English: audit and fixes (22 Oct 2026)

The maths fix brief (`One_Hundred_Maths_Audit_v1`) applied to the English app (grammar, punctuation and
spelling, 37 subtopics). It followed the same four phases. The English app shares the maths shell, so it had
the same shell faults, plus faults of its own that mattered more for learning.

Checked at 390 × 844 in Playwright before each commit. Generator output (what is asked and what is accepted)
was recorded for 300 seeds per generator before any change and compared after every phase.

## What was wrong

### Lessons did not match their subtopics
Lessons were stored one per question generator, and one generator serves many subtopics:

| Subtopics | Lesson every one of them showed |
|---|---|
| 11 spelling subtopics (silent letters, homophones, ough, ...) | "endings that sound like shun" |
| Commas and brackets, Semi-colons and dashes, Colons, Hyphens | paired commas |
| Nouns, Verbs, Adjectives, ... Conjunctions (8) | one shared word-class lesson |

So 19 lessons served 37 subtopics, and 23 subtopics taught something else.

### Questions that could not teach
- **Punctuation:** the only tappable gap was the right one, so one tap always scored.
- **Punctuation subtopics:** practice drew all six kinds, so "Colons" asked about brackets and hyphens.
- **"The underlined part is a…":** nothing was underlined.
- **Tense:** sentences had two blanks but only one answer box.
- **Spelling bank:** "four" was the answer to "We used plain ___ to make bread". "suggestion" and "solution"
  shared one sentence.

### The same shell faults as maths
- A video placeholder with a file name, and made-up timecodes, on every lesson. The cover claimed "19 short
  videos" when there were none.
- Titles hidden under the header. A floating back button covering answers.
- Lesson order: the bare steps came first ("not for learning from"), then an apology, then the teaching.
- "Show me the answer" printed the answer and nothing else. Every hint was step one of the lesson.

### Language
Sentence length was already short (Flesch-Kincaid about grade 3). The difficulty was elsewhere:
- **Metaphors:** "Punctuation is not decoration", "the name of the job, not the name of the word", "a
  dial for how certain something is".
- **Terms used without definitions:** subordinate, relative, determiner, progressive, perfect.
- **Fear words:** "trap", "catches people out", "costs the mark".
- **Plain names instead of test terms:** "Shortened words" rather than *contractions*, "Words that mean the
  same" rather than *synonyms*.
- **No sign of what the test question would look like.**

## What changed

| Phase | Version | Change |
|---|---|---|
| 1 | v11 | Shell fixes as in maths (no video talk, header, back button, teaching-first lesson, steps in practice, hint at the top). Lessons routed per subtopic. Punctuation practice limited to the subtopic's marks. A gap between every pair of words. The underline drawn. One blank per tense question. "flour" in place of "four". |
| 2 | v12 | Every question explains its answer: a "Why" box that keeps the question and puts the answer into it. Hints match the mistake made, for example "That word means the opposite. You need a word that means the same." Typed answers are checked for the usual slips: a missing apostrophe, no was/were, a right start but the wrong ending. |
| 3 | v13 | Pictures for English: the sentence marked as a teacher marks it on the board (highlight, underline, cross out, insert, labels), built up step by step. A scale model (when it happens, how sure). Word-building blocks (prefix + root, root + suffix, do + not). Each question gets a drawing of its own words on the first two questions. |
| 4 | v14 | 37 lessons, one per subtopic, laid out by a learning-design template (below). Six subtopic names changed to the test terms. |

### The lesson template (every subtopic)
1. **In the test:** the question as the paper words it ("Insert a semi-colon in the correct place.").
2. **Key words:** the test term in bold, with a plain definition that reads as one sentence.
3. **Why it matters:** one or two short, concrete situations.
4. **Worked example:** steps revealed one at a time. The marked-up sentence redraws for each step, and
   tapping a step opens its reason. Every reason says what to do.
5. **Another one:** a second worked example, folded away, which changes the one thing that usually trips
   children up.
6. **In the test:** a test-style question, with the working behind "Show me how" so the child tries it first.
7. **Spot the mistake:** tap the wrong line, then see the fix. It is not scored.
8. **Try one with me**, then practice.

### Language grading used
- National Curriculum Year 6 terms, exactly as the test uses them. Each is defined the first time it appears.
- One idea per sentence. The lesson prose averages 7 words a sentence: 3 of 1 500 sentences go over 18
  words, two of them because they contain a quoted example.
- No metaphors or idioms. No fear words; say what to do instead.
- Examples from school and home, with varied names and UK spelling.
- The SATs question words: Tick one, Circle, Underline, Insert, Write.

## Not done, for the owner
- **Audio:** spelling still uses the phone's voice (`AUDIO` is empty). Recordings are the biggest remaining
  gap for the spelling paper.
- **Videos:** there are none. When they are recorded, they should follow the new lessons.
- **French:** the app reads only English (`L` is fixed). No French was added, and the old French strings in
  removed lessons went with them.
- **The S41 bank includes "increase":** its in- is not the negative prefix the lesson teaches. Consider
  replacing it.
- **Reading comprehension** is still out of scope, as the README says.
