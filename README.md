# Data Labelling Lab

## Overview
This lab demonstrates two approaches to data labeling in MLOps:
1. **Manual Labeling** using Label Studio
2. **Programmatic Labeling** using Snorkel (Weak Supervision)

---

## Part 1 - Manual Labeling with Label Studio

### What I did
Used Label Studio to manually annotate a custom movie review dataset for binary sentiment classification.

### Dataset
- File: `movie_reviews.csv`
- 20 movie reviews
- Labels: Positive / Negative

### Output
- File: `annotations.json` — exported labels from Label Studio

---

## Part 2 - Programmatic Labeling with Snorkel

### What I did
Used Snorkel's weak supervision framework to automatically label a custom spam detection dataset using labeling functions.

### Dataset
- File: `custom_spam_dataset.csv`
- 20 messages (spam/ham)
- Labels: SPAM=1, HAM=0

### Labeling Functions Used
- `lf_contains_link` — detects URLs and "click here"
- `lf_contains_free` — detects free offers
- `lf_contains_win` — detects winning messages
- `lf_contains_urgent` — detects urgency words
- `lf_contains_money` — detects money related words
- `lf_normal_conversation` — detects normal messages

### Results
- Model Accuracy: **80%**
- Spam detected: 8
- Ham detected: 8

### Output
- File: `01_spam_tutorial_custom_dataset.ipynb` — Snorkel spam tutorial notebook

---

## Tools Used
- Label Studio
- Snorkel
- Python, Pandas, Jupyter Notebook

## References
- [Snorkel Tutorials](https://github.com/snorkel-team/snorkel-tutorials)
- [Label Studio](https://labelstud.io/)
