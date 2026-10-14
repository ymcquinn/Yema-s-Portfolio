# Movie Genre Classification from Plot Summaries

Predicting genre from plot text using the CMU Movie Summary Corpus.

## Dataset
- 42,306 movies with plot summaries + Freebase metadata
- Curated to 8 clean genres: Drama, Comedy, Romance, Action, Thriller, Horror, Sci-Fi, Crime
- Final corpus: 34,770 movies

## Approach
- **Vectorization:** TF-IDF, 20k features, unigrams, sublinear TF
- **Supervised:** Logistic Regression vs. Multinomial Naive Bayes (10-fold stratified CV, macro F1)
- **Unsupervised:** KMeans on SVD-reduced vectors (100 components)
- **Topic modeling:** LDA (10 topics) with pyLDAvis visualization

## Results

| Model | Accuracy | Precision | Recall | Macro F1 |
|---|---|---|---|---|
| Logistic Regression | 0.529 | 0.488 | 0.516 | **0.498** |
| Naive Bayes | 0.472 | 0.586 | 0.262 | 0.254 |

- **KMeans** (ARI 0.044): recovered interpretable Sci-Fi, Crime/Thriller, and Romance-Drama clusters despite low label-alignment.
- **LDA** (10 topics): surfaced *production clusters* (animation, Bollywood, East Asian cinema) rather than editorial genres — a genuinely interesting finding.

## Key insight
Genre is a **supervised editorial category**, not a latent property of plot text. Clustering and topic modeling reveal thematic structure that only partially aligns with genre labels. The Q1 confusion matrix (Drama ↔ Romance: 2,778 errors; Comedy ↔ Drama: 1,979 errors) confirms this semantic overlap.

## Stack
Python · scikit-learn · Gensim · pyLDAvis · pandas · matplotlib
