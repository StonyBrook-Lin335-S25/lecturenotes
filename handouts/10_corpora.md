---
title: Computational Linguistics Handout
author: Thomas Graf
date: 2025-02-23
geometry: margin=1in, letterpaper
fontsize: 12pt
numbersections: true
fontfamily: mathdesign
fontfamilyoptions: charter
---

**Disclaimer**  
These handouts serve as a succinct reference of what was covered in a given class.
They are not meant to be a substitute for attending class and probably won't make much sense to you unless you were there.

# Corpora

- Ever since the probabilistic turn, computational linguistics has had a big need for data.
- This data comes in the form of **corpora**.
- A **corpus** is a collection of data, usually written text.

# Differences between corpora

- Languages
    - corpora exist for many languages
    - of course very common languages (English, Arabic, Chinese) have more corpora than smaller ones (e.g. Finnish)
    - both the number of corpora and the size of those corpora tends to scale with how much of a market there is for language technology in that language
    - Dialect and sociolect corpora are exceedingly rare, e.g. for African American Vernacular English (AAVE) or for non-standard Arabic
- License
    - free or do you have to pay?
    - can you use it for commercial products or only for research?
- Register
    - what kind of language is this?
    - *Examples*: news paper articles, emails, spoken conversations
- Curation
    - Has the data in the corpus been checked and cleaned up by a human?
    - *Example*: you can build a corpus by automatically collecting tweets, but there's probably a lot of crud in there
- Annotation
    - is it just the raw linguistic data (words, sentences) or is there additional information
    - **Tree bank**: a corpus where each sentence is annotated with a tree that encodes its syntactic structure
    - *Examples*: parts-of-speech, morphological information (person and number, tense), information about the source of a sentence (age and gender of speaker)

# What kind of corpus do you want?

- Since annotating and checking data takes time and resources, there's always a trade-off between corpus size and corpus quality.
- One reason neural networks have been so successful is that they perform so well when trained on cheap data.
  No annotations, no human sanity-checking, just tons and tons of freely available data from the internet.
- This is a big difference to the models from the 90s, which required high-quality data.

# Examples of corpora

- All of the corpora below are available in NLTK
- To install all NLTK corpora (about 2GB)

```python
import nltk
nltk.download("all")
```

- Working with a corpus `foobar`

```python
# load the corpus
from nltk.corpus import foobar

# look at what's in it
foobar.words()

# look at the 173rd word
foobar.words()[173]
```


## Penn Treebank

```python
from nltk.corpus import treebank
```

- the most-used treebank in the world
- Language: English
- not free, NLTK only contains a small sample
- built from articles in the WSJ
- each sentence annotated with tree structures
    - annotated by multiple independent annotators, then checked for conflicts

## Brown corpus

```python
from nltk.corpus import brown
```

- built from text published in 1961
- about 1 million words
- contains a variety of genres: news paper articles, fiction, scientific writing, and more
- includes part-of-speech tags

## Switchboard corpus

```python
from nltk.corpus import switchboard
```

- spoken corpus
- 2,400 telephone conversations, total of 260 hours
- NLTK only includes the transcriptions

## Stopword corpus

```python
from nltk.corpus import switchboard
```

- unique to NLTK, this is simply a list of stopwords in a variety of languages

## Carnegie Mellon Pronouncing Dictionary

```python
from nltk.corpus import cmudict
```

- a list of English words with their pronunciations
- pronunciations use a modified form of [ARPABET](https://en.wikipedia.org/wiki/ARPABET)

## Wordnet

```python
from nltk.corpus import wordnet
```

- This isn't so much a corpus as a database of word meanings and how words are related to each other
