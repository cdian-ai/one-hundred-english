# One Hundred — English

Year 6 SATs English: grammar, punctuation and spelling. Ages 9 to 11.
One HTML file, no build step, no backend. English and French.

Companion to [ks2-maths](https://github.com/cdian-ai/ks2-maths) — same shell,
same cover, same subtopic page, so the two read as one product.

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

Every subtopic has its own lesson, laid out the same way: what the test
question looks like, the key words with plain definitions, why it matters, a
worked example built up step by step on a marked-up sentence, another example,
a test-style question, and a mistake to spot. Then one done together, then
practice. In practice the steps are a tap away, a wrong answer gets a hint
about the mistake made, and "Show me the answer" says why. When a video
exists it plays first and the written lesson sits behind "Read it instead".
See `docs/one-hundred-english-audit-2026-10-22.md`.

    VIDEO.apostrophe = { en:"vid/apostrophe-en.mp4", fr:"vid/apostrophe-fr.mp4" };

## Still to do

- Record the videos: 17 subtopic explainers × 2 languages
- Spelling needs audio — 20 words a paper, single words, not sentences. The
  same recording rig as the Fulfulde course covers it.
- The app has the same placeholder-free name as the maths one, but the pair
  needs a shared publisher identity if both go into Notice Me.
