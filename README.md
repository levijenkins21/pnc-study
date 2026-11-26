# Life & Health Licensing Exam Study Site

Static study site for the Kansas Life & Health insurance license exam. Practice-test focused with a reusable quiz engine, missed-questions deck, timed practice exams, and score tracking.

**Live site:** https://levijenkins21.github.io/pnc-study/

## Exam Info

Kansas exams (Pearson VUE, handbook #121700 July 2026):

- **Life Producer (12-KS-01):** 84 scored + 11 pretest questions · 90 minutes · 70% to pass
- **Life & Accident/Health (12-KS-05):** 140 scored + 14 pretest questions · 150 minutes · 70% to pass

## Features

### Practice Tools

- **Missed Questions Deck** — Every wrong answer automatically saved for review
- **Timed Practice Exam** — Real exam conditions with countdown timer
- **Score History** — Track progress across all quizzes and exams
- **Continue Studying** — Dashboard remembers your last page

### Chapter Content

- Lesson slides (concept walkthroughs)
- Flashcards with section filtering and progress tracking
- Chapter quizzes that feed the missed-questions deck

## Current Content

- **Chapter 9:** Kansas Statutes Common to All Lines (21 questions)
  - Lesson (19 slides)
  - Flashcards (52 cards)
  - Quiz (21 questions)

All other chapters show "Coming soon" and will appear as content is added.

## Adding New Chapters

1. Add the chapter's question bank to `question-banks.js`:

```javascript
window.QUESTION_BANKS['LH_Ch10'] = [
  { s:"Section", q:"Question text", choices:["A","B","C","D"], correct:1, explain:"Explanation" },
  // ...
];
```

2. Create the chapter files:
   - `LH_Ch10_Lesson.html`
   - `LH_Ch10_Flashcards.html`
   - `LH_Ch10_Quiz.html`

3. The dashboard automatically detects new files and displays them.

## localStorage Keys

Life & Health uses `lh_*` keys (separate from P&C's `pc_*` keys):

- `lh_last_page` — Resume feature
- `lh_missed` — Missed questions deck
- `lh_score_history` — Quiz/exam results
- Chapter-specific progress (flashcards, etc.)

## P&C Archive

The original P&C study site has been moved to `/pc/` and is fully functional at:

https://levijenkins21.github.io/pnc-study/pc/PC_Dashboard.html

A link to it appears on the Life & Health dashboard.

## Design

Clean, dark, Linear-style UI. Inter font, single accent color (#5b8dee), thin borders, generous spacing. Mobile-first responsive design.

## Tech Stack

Plain static HTML/CSS/JS. No build step. No backend. Works on GitHub Pages.
