# IMDB Sentiment Classifier – Film Junky Union

This project builds a machine learning classifier to automatically detect **negative movie reviews** from a dataset of IMDB reviews. Created as part of the Film Junky Union initiative, this tool helps filter and analyze large volumes of user-submitted reviews to improve community moderation and content tagging.

---

## Table of Contents

- [Dataset](#dataset)
- [Objective](#objective)
- [Models Trained](#models-trained)
- [Evaluation](#evaluation)
- [Final Verdict](#final-verdict)
- [Project Structure](#project-structure)

---

## Dataset

- **Source**: [Maas et al., ACL 2011](https://ai.stanford.edu/~amaas/data/sentiment/)
- **File**: `imdb_reviews.tsv`
- **Size**: ~47,000 reviews
- **Fields**:
  - `review`: Full review text
  - `pos`: Sentiment label (0 = Negative, 1 = Positive)
  - `ds_part`: Dataset partition (`train` or `test`)

---

## Objective

Train and evaluate models to:
- Classify reviews as **positive** or **negative**
- Achieve a minimum **F1 score ≥ 0.85**
- Compare performance across models and on real-world custom reviews

---

## Models Trained

| Model               | F1 Score | Accuracy |
|--------------------|----------|----------|
| Logistic Regression| **0.885** | 88.5%    |
| XGBoost            | 0.860    | 85.8%    |
| LinearSVC          | 0.868    | 86.9%    |

All models exceeded the F1 target.

---

## Evaluation

- Custom user-written reviews tested against all models
- Confusion matrices used to visualize performance
- Logistic Regression showed best balance of precision/recall

---

## Final Verdict

**Logistic Regression** is the recommended model for deployment:
- Fast, simple, and effective
- Best performer on both test and real-world data
- No additional tuning required

---

## Project Structure

```bash
.
├── imdb_reviews.tsv         # Dataset
├── sentiment_classifier.ipynb  # Jupyter Notebook
├── README.md                # Project description
