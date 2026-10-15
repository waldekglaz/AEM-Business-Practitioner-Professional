# AEM Business Practitioner Mock Exam

A practice exam for the **Adobe Experience Manager Business Practitioner Professional** certification (exam **AD0-E138**). It's one self-contained HTML file with no build step and no dependencies.

> **Unofficial study aid.** This project isn't affiliated with or endorsed by Adobe. The questions are original and written against Adobe's published exam objectives. They aren't questions from the real exam. AEM changes often, so check anything that looks off against the Adobe documentation linked from each answer.

## Using it

Open `index.html` in a browser. To host it, publish the repository with GitHub Pages (Settings → Pages → deploy from the `main` branch).

- **Full exam:** 50 questions drawn by the official section weights, a 100-minute timer, flagging and a question navigator. You need 30 correct answers to pass.
- **Practice:** choose sections and check each answer as you go. You get an explanation and a documentation link, with no timer.
- **Results:** your score against the pass mark, a score for each section, and a review of every question that you can filter to missed or flagged ones.
- **Keyboard:** <kbd>A</kbd>–<kbd>D</kbd> choose an answer, <kbd>N</kbd> next, <kbd>P</kbd> previous, <kbd>F</kbd> flag.

An exam in progress and your past attempts are saved in your browser's `localStorage` only.

## Exam blueprint

The sections and weights come from [Adobe's AD0-E138 certification page](https://certification.adobe.com/certification/business-practitioner-professional-v2/539): 50 scored questions, 100 minutes, 30 correct to pass. Adobe may add up to 10 unscored questions.

| Section | Weight | Questions per mock exam | Questions written |
|---|---|---|---|
| 1. Product Capabilities | 28% | 14 | 28 |
| 2. Content Authoring and Optimization | 24% | 12 | 23 |
| 3. Technical | 16% | 8 | 20 |
| 4. Content Delivery | 22% | 11 | 20 |
| 5. Business Analysis | 10% | 5 | 10 |

## Adding or fixing questions

The questions live in the `QUESTIONS` array near the top of the `<script>` in `index.html`:

```js
{ id: "P05", o: "1.1",                 // unique id, objective from OBJECTIVES
  q: "Question text, `inline code` allowed",
  opts: ["Correct answer", "Distractor", "Distractor", "Distractor"],
  a: [0],                              // indexes of the correct options; two or more makes it a "choose N" question
  ex: "Why the answer is right.",
  ref: ["Link title", "https://experienceleague.adobe.com/..."] }
```

Answer options are shuffled on every attempt, so the correct one can be listed first.
