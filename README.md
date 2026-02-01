# Text_as_data_HM1
# IDS 570 – Homework 1  
**Text as Data | Word Frequencies and Normalization**

This repository contains my submission for **Homework 1** of *IDS 570: Text as Data*.  
The assignment extends the Week 02 word frequency analysis by accounting for **document length** through **relative (normalized) frequencies**.

---

## Contents

- `Homework1.qmd`  
  Quarto source file containing all code and analysis.

- `Homework1.html`  
  Rendered HTML output with tables and visualizations.

- `texts/`  
  Folder containing the two source texts:
  - *Text A*: Circle of Commerce  
  - *Text B*: Free Trade

---

## What This Assignment Does

### 1. Corpus Diagnostics (Before Stopword Removal)
- Computes a diagnostics table with one row per document:
  - Number of characters (`n_chars`)
  - Number of word tokens (`n_word_tokens`)
  - Number of unique word types (`n_word_types`)
- Used to assess whether the two texts are comparable in length.

### 2. Word Counts After Stopword Removal
- Tokenizes texts using `tidytext`
- Lowercases all tokens
- Removes stopwords (built-in + custom list)
- Produces raw word counts per document

### 3. Normalization by Document Length
- Computes total number of words per document after stopword removal
- Normalizes word counts to relative frequencies:
  
  \[
  \text{relative frequency} = \frac{n}{\text{total words in document}}
  \]

### 4. Comparing “trade” Across Texts
- Reports raw counts and relative frequencies for the word **“trade”**
- Demonstrates how normalization changes interpretation compared to raw counts

### 5. Normalized Top-20 Word Visualization
- Recreates the Week 02 Top-20 word frequency plot
- Uses **relative frequencies instead of raw counts**
- Displays side-by-side faceted bar charts for Text A and Text B

---

## Interpretation (Posted on Canvas)

Short prose interpretations addressing:
- Whether Text A and Text B are comparable in length
- Implications for raw frequency comparisons
- Whether “trade” is used more proportionally in one text
- How results would differ if normalization were done *bef*
