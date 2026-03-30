Pakistan Financial Sentiment & Equity Dataset (2025–2026)
=========================================================

**Project Overview**
--------------------

This dataset was developed to investigate the correlation between social media discourse and the Pakistani equity market. It focuses specifically on the Oil & Gas Development Company (OGDC) and sentiment gathered from regional financial communities. The dataset bridges a critical gap in available localized financial data for the Pakistan Stock Exchange (PSX).
It was manually curated to analyze the relationship between social media sentiment and the Pakistani equity market (specifically OGDC). It bridges a gap in available data by aggregating local Reddit discourse, financial news, and stock prices into a unified time-series format.

**1\. Data Sources & Structure**
--------------------------------

### **Primary Sentiment Corpus (2025–2026)**

*   **Reddit (NDJSON):** r/pakistan, r/FIREPakistan, and r/pakistanfinance.
    
*   **Processing:** Records were extracted, cleaned of noise/bots, and aggregated daily.
    
*   **Metric:** Includes daily sentiment scores using both **VADER** and **Loughran-McDonald (L-M)** lexicons.
    

### **Financial Target Variable**

*   **OGDC Prices:** Historical daily price and volume data for OGDC, aligned to 247 overlapping trading days within the analysis window.
    

### **Validation & Supplementary Data**

*   **Financial PhraseBank:** 5,842 human-labeled sentences used to empirically validate lexicon accuracy.
    
*   **RSS News:** Supplementary text data from financial news feeds.
    
*   **WSB Dataset (Kaggle):** Historical WallStreetBets data (Sep 2020 – Aug 2021).
    
    *   _Note:_ This is included for **baseline sentiment distribution analysis** but was excluded from the final time-series model due to zero temporal overlap with the 2025–2026 PSX price window.
        

**2\. Directory Structure**
---------------------------

The dataset follows a standardized data engineering pipeline:

*   data/raw/: Original, untouched source files (NDJSON, CSV, RSS).
    
*   data/interim/: Intermediate files post-cleaning and timestamp normalization.
    
*   data/processed/: The final analytical files used for modeling.
    
    *   all\_reddit\_pk\_daily.csv: The core daily sentiment features.
        
    *   ogdc\_prices\_clean.csv: Cleaned and aligned market data.
        
*   scripts/: Python scripts used for ETL (Extraction, Transformation, Loading) and sentiment scoring.
    

**3\. Methodology & Validation**
--------------------------------

*   **Data Integrity:** All text underwent rigorous normalization, including emoji removal, case-sensitivity handling for VADER, and date standardization.
    
*   **Lexicon Performance:** Through the Financial PhraseBank validation, the **L-M lexicon** was found to outperform VADER by **5.8 percentage points** on financial-specific text, justifying its weight in the final analysis.
    
*   **Temporal Alignment:** The dataset provides **247 overlapping trading days**, covering a full year of market activity.Pakistan Financial Sentiment & Equity Dataset (2025–2026)
=========================================================

**Project Overview**
--------------------

This dataset was developed to investigate the correlation between social media discourse and the Pakistani equity market. It focuses specifically on the Oil & Gas Development Company (OGDC) and sentiment gathered from regional financial communities. The dataset bridges a critical gap in available localized financial data for the Pakistan Stock Exchange (PSX).

**1\. Data Sources & Structure**
--------------------------------

### **Primary Sentiment Corpus (2025–2026)**

*   **Reddit (NDJSON):** Scraped from r/pakistan, r/FIREPakistan, and r/pakistanfinance.
    
*   **Processing:** Records were extracted, cleaned of noise/bots, and aggregated daily.
    
*   **Metric:** Includes daily sentiment scores using both **VADER** and **Loughran-McDonald (L-M)** lexicons.
    

### **Financial Target Variable**

*   **OGDC Prices:** Historical daily price and volume data for OGDC, aligned to 247 overlapping trading days within the analysis window.
    

### **Validation & Supplementary Data**

*   **Financial PhraseBank:** 5,842 human-labeled sentences used to empirically validate lexicon accuracy.
    
*   **RSS News:** Supplementary text data from financial news feeds.
    
*   **WSB Dataset (Kaggle):** Historical WallStreetBets data (Sep 2020 – Aug 2021).
    
    *   _Note:_ This is included for **baseline sentiment distribution analysis** but was excluded from the final time-series model due to zero temporal overlap with the 2025–2026 PSX price window.
        

**2\. Directory Structure**
---------------------------

The dataset follows a standardized data engineering pipeline:

*   data/raw/: Original, untouched source files (NDJSON, CSV, RSS).
    
*   data/interim/: Intermediate files post-cleaning and timestamp normalization.
    
*   data/processed/: The final analytical files used for modeling.
    
    *   all\_reddit\_pk\_daily.csv: The core daily sentiment features.
        
    *   ogdc\_prices\_clean.csv: Cleaned and aligned market data.
        
*   scripts/: Python scripts used for ETL (Extraction, Transformation, Loading) and sentiment scoring.
    

**3\. Methodology & Validation**
--------------------------------

*   **Data Integrity:** All text underwent rigorous normalization, including emoji removal, case-sensitivity handling for VADER, and date standardization.
    
*   **Lexicon Performance:** Through the Financial PhraseBank validation, the **L-M lexicon** was found to outperform VADER by **5.8 percentage points** on financial-specific text, justifying its weight in the final analysis.
    
*   **Temporal Alignment:** The dataset provides **247 overlapping trading days**, covering a full year of market activity.