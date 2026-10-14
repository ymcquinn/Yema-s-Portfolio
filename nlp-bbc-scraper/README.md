# BBC News Scraper & NLP Preprocessor

Web-scraping pipeline that extracts clean article text from live HTML and processes it through a full NLP preprocessing stack.

## Pipeline

1. Fetch HTML from a live BBC News URL (custom User-Agent to bypass blocking)
2. Parse with BeautifulSoup, extract only `<p>` tags to isolate article body
3. Normalize whitespace with regex
4. Tokenize into sentences (`sent_tokenize`) and words (`word_tokenize`)
5. Filter meaningful tokens (alphabetic only)
6. Remove English stopwords
7. Part-of-speech tag the first 5 sentences using NLTK's Penn Treebank tagset

## Output
- Meaningful tokens: 350
- Sentences: 20
- Stopwords encountered: 150 (42.86% of tokens)
- First 5 sentences POS-tagged

## Stack
Python · NLTK · BeautifulSoup · requests
