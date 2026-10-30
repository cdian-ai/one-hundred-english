# One Hundred — English

Year 6 SATs English: grammar, punctuation and spelling. Ages 9 to 11.
One HTML file, no build step, no backend. English and French.

Companion to [ks2-maths](https://github.com/cdian-ai/ks2-maths) — same shell,
same cover, same subtopic page, so the two read as one product.

## v2: the Woven design, and Reading (October 2026, branch `v2-woven-design`)

Rebuilt in the same design as One Hundred Maths v2 (indigo for English, Nuuru in
the English hat, Nunito): Home with six topic tiles and ten blocks each (block 8
is the "ready" line), topic and part pages, the daily ten, a forgiving streak,
Ready for SATs, For parents and Mocks. English only for now; the French text is
still in the data.

- **Six topics, 58 parts**: Word classes, Sentences & clauses, Verbs, tenses &
  Standard English, Punctuation, Spelling & vocabulary, and **Reading**. The 37
  original subtopics are reused; about 20 grammar and punctuation areas that were
  missing now have practice (subject and object, question tags, relative clauses,
  present perfect, progressive, subjunctive, speech, bullet points and more).
- **Every word is tappable** in "tap the noun" questions (before, only the right
  words were buttons, which gave the answer away), and punctuation questions put
  a gap between every pair of words (before, every gap was a right one).
- **The Year 3–6 word lists**, all read aloud in a sentence, and bigger banks.
- **Reading**, with texts written for the course (a story, a non-fiction text
  about wells, and a poem), questions on all eight skills (2a–2h), and the long
  answers compared with a full-mark answer and self-marked.
- **Three mocks**: grammar and punctuation (50 questions, 45 min), spelling (20
  words read aloud) and reading (all three texts, 60 min).
- **Video scripts v2**: `scripts/ks2-english-video-scripts-v2-2026-10-30.csv`,
  38 films covering the parts (parts that teach the same method share a film).

## What it is built from

The **2024, 2025 and 2026 mark schemes** — 150 questions, each tagged by the
Standards and Testing Agency with the content domain it assesses.

Two findings shaped the whole build:

- **Spelling is the biggest single part of the test.** 20 of the 70 marks, more
  than punctuation. Looking at Paper 1 alone hides this. It gets 11 subtopics.
- **The domain is almost closed.** 50 codes exist; **43 appear in all three
  years** and account for 94% of every question asked. You can honestly tell a
  child there are about 43 things on this paper and here they all are. No maths
  app can say that.

Share of the whole 70-mark test:

| | |
|---|---|
| Spelling | 29% |
| Punctuation | 21% |
| Word classes | 19% |
| Verbs and tense | 9% |
| Clauses and phrases | 7% |
| Vocabulary | 7% |
| Standard English | 4% |
| Kinds of sentence | 4% |

## What is not here

**Reading comprehension.** That is the third paper, 50 marks, and it is a
different product: it needs licensed texts and hand-marked answers, neither of
which this engine does. The app says GPS and covers GPS.

## How it works

8 topics, 37 subtopics, 352 questions. Four ways to answer, matching the real
paper: tap the words, tap where the punctuation goes, choose one, or write it.
No keypad — this is not maths.

Video first, with a jump index into it per step; a quick reminder card for
checking mid-question; then practice. Until a film exists the full written
explanation shows instead.

    VIDEO.apostrophe = { en:"vid/apostrophe-en.mp4", fr:"vid/apostrophe-fr.mp4" };

## Still to do

- Record the videos: 17 subtopic explainers × 2 languages
- Spelling needs audio — 20 words a paper, single words, not sentences. The
  same recording rig as the Fulfulde course covers it.
- The app has the same placeholder-free name as the maths one, but the pair
  needs a shared publisher identity if both go into Notice Me.
