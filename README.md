# Sentiment Analysis of Song Lyrics Across Music Corpora (VADER)

This repository contains the data, code, and results of a sentiment analysis conducted on lyrics from four music corpora (**The Beatles, CSNY, Grunge, and SNA**). The core goal of this project is to demonstrate lyric sentiment by performing a **quantitative comparative analysis** of the emotional tone across these music corpora. The project utilizes the **VADER (Valence Aware Dictionary and sEntiment Reasoner) [1]** model to derive robust, aggregated sentiment scores.

---

## VADER Sentiment Analysis

The analysis relies on the VADER (Valence Aware Dictionary and sEntiment Reasoner) model, a powerful tool built on a **lexicon-and-rule-based architecture** highly adapted to analyzing informal and colloquial language.

- **Compound Score**: VADER’s primary metric is the normalized, weighted sum of sentiment ratings of the words in the text.  
  - Range: **−1 (extremely negative) to +1 (extremely positive)**  
- **Overall Sentiment Score** for each corpus is calculated by taking the **arithmetic mean** of all individual song Compound Scores within that group.

The final average score is classified using standard VADER thresholds:

- **≥ 0.05** → Positive  
- **≤ −0.05** → Negative  
- **Between −0.05 and 0.05** → Neutral  

---

## Project Structure

```
├── code/                         # Analytical Jupyter Notebook
│   └── VADER_Sentiment_Analysis.ipynb
│
├── data/                         # Input CSV files for the four corpora
│   ├── beatles.csv
│   ├── csny.csv
│   ├── grunge.csv
│   └── sna.csv
│
└── README.md
```

---

## How to Run

To reproduce the workflow, follow these steps:

1. **Download** the repository folder to your local machine.  

2. **Install prerequisites**:  

   ```bash
   pip install pandas nltk jupyter pathlib
   ```

   > Note: The VADER model is a module of the **Natural Language Toolkit (NLTK)**.

3. **Execution**:
   - Navigate to the project’s root directory.  
   - Start the Jupyter environment:  

     ```bash
     jupyter notebook
     ```  

   - Open the file `code/VADER_Sentiment_Analysis.ipynb` and run all cells sequentially.  

---

## Reference

[1] C. J. Hutto, E. E. Gilbert, *VADER: A parsimonious rule-based model for sentiment analysis of social media text*, Proceedings of the International AAAI Conference on Web and Social Media. 8 (2014) 216–225. https://doi.org/10.1609/icwsm.v8i1.14550.
