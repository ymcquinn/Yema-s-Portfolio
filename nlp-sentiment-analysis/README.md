# Lexicon-Based Sentiment Analysis

Sentiment classification of NYTimes articles using NLTK's Hu & Liu opinion lexicon.

## Approach

- **Lexicon:** Hu & Liu opinion lexicon (positive and negative word lists)
- **Preprocessing:** Tokenization, lowercasing, POS tagging, regex-based pattern matching
- **Extraction:** Handled multiple source formats — HTML, PDF, and plain text — using BeautifulSoup, inscriptis, and NLTK's CorpusReader
- **Classification:** 0–5 positivity scale based on lexicon overlap

## Stack
Python · NLTK · BeautifulSoup · inscriptis
