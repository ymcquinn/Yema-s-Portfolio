# NLP Corpus Vectorization Pipeline

End-to-end normalization and vectorization of a 3,134-document nested corpus.

## Pipeline

1. **Load** — nested structure: documents → paragraphs → sentences → (word, POS-tag) tuples, read from pickled MongoDB-style exports
2. **Normalize** — custom sklearn `NormalizationTransformer`: skip metadata paragraphs, lowercase, strip punctuation, drop stopwords, Porter-stem
3. **Vectorize** — Gensim TF-IDF (dictionary: 41k → 12k features after `filter_extremes`) and Doc2Vec (100-dim embeddings, Distributed Memory)

## Verification

The Doc2Vec embeddings were validated without supervision: the top-5 most similar documents to Document 0 were all in the same category, confirming the model learned category-discriminative representations from text alone.

## Corpus

- 3,134 documents across two categories (books, cinema)
- 1.2 million tokens after normalization (~387 per document)
- Handled upstream contamination: MongoDB JSON metadata paragraphs and whitespace-escape artifacts

## Stack
Python · Gensim · NLTK · scikit-learn
