# Writeup Review — TODO Checklist

## Critical Fixes

- [ ] **Add LLM usage disclosure** — project rules require explaining how you used GPT-4/LLMs
- [ ] **Fill or delete empty `Arg Max` section** (line 101) — likely intended to show the final argmax decision combining prior + likelihoods
- [ ] **Fix dataset size** (line 251) — says "100 deepfakes and 100 real" but actual is 200 real + 200 deepfake (400 total), ~320 train / 80 test
- [x] **Fix math typo** (line 30) — `P(Y = | X = X)` → `P(Y = y | X = x)`

---

## Unfilled Placeholders

- [ ] Line 18 — `(I wonder what's the percentage is???)` — find a stat or remove
- [ ] Line 18 — `\footnote{Find Link}` for LeBron video — add link or remove
- [x] Line 18 — `\footnote{Heres a deepfake I made...}` — cleaned up to descriptive text
- [x] Line 21 — `\footnote{add their citation}` for FaceForensics++ — Rössler et al., ICCV 2019
- [x] Line 24 — `\footnote{what is DCT}` — added brief explanation
- [x] Line 24 — `\footnote{what is MAD}` — added brief explanation
- [x] Line 65 — `\footnote{link to gamma}` — added explanation + Wikipedia link
- [x] Line 99 — `\footnote{Here is a link to how scipy implements it}` — added scipy docs URL
- [x] Line 123 — `\footnote{link to gradient descent explanation}` — added explanation with update rule
- [x] Line 228 — `\footnote{What is ROC?}` — added explanation of TPR/FPR curve
- [x] Line 234 — `\footnote{What is f5 again?}` — added definition + appendix reference
- [x] Line 234 — `\footnote{What metric}` — specified AUC with value
- [x] Line 55 — `\footnote{what does this mean}` for monotone function — added explanation with argmax equivalence

---

## Typos & Grammar

- [x] Line 18 — "aceswaps" → "faceswaps"
- [x] Line 18 — "english teacher" → "English teacher"
- [x] Line 21 — "Generative Adversial" → "Generative Adversarial"
- [x] Line 46 — "are data" → "our data"
- [x] Line 55 — "likehood" → "likelihood"
- [x] Line 131 — "independance" → "independence"
- [x] Line 158 — "it's output probabilities" → "its output probabilities"
- [x] Line 240 — "it's higher AUC" → "its higher AUC"

---

## Structure & Content

- [x] **Move KDE section** — currently nested under Logistic Regression but KDE is used in Naive Bayes; move it there or make it top-level
- [x] **Anchor Youden's J** — it floats without a clear parent section; make it a subsection of Naive Bayes or Results
- [ ] **Explain why logistic regression handles correlated features better** — NB's independence assumption causes double-counting; logistic regression learns a single linear boundary without that assumption
- [x] **Add baseline comparisons to results tables** — random (≈50%), majority-class added to both tables with a second \hline
- [x] **Add ROC curve figure** — added roc_comparison_all_methods.png (all methods), score_distribution_f5.png, and segmentation_test.png; clearpage added to keep figures before Future section
- [x] **Write the features appendix** — ✅ Done

---
a
## Nice to Have

- [ ] Add a short **Dataset section** — describe FF++, why c0 vs c23 matters, 200+200 split
- [ ] Switch to **BibTeX** for citations instead of footnotes (at minimum for FF++)
- [ ] Add a feature distribution plot for a second feature to illustrate NB degradation with correlated features
- [x] Add a **ROC comparison plot** (f5-only vs all-features) — done via roc_comparison_all_methods.png
- [ ] Tighten tone consistency — intro is casual with unfinished thoughts; decide on a voice and clean up
