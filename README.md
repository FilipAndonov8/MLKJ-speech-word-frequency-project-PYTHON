# MLK Speech Word Frequency Analysis — Web Scraping & Regex

## Overview
This project scrapes the full text of Martin Luther King Jr.'s "I Have a Dream" speech from the web, cleans and processes the text using regular expressions, and produces a word frequency count — a small end-to-end text analysis pipeline using Python.

## What It Does
1. **Scrapes** the speech text from a public webpage using `requests` and `BeautifulSoup`
2. **Cleans** the text: removes line breaks, strips punctuation using regex, and converts everything to lowercase
3. **Tokenizes** the cleaned text into individual words using regex (`re.split`)
4. **Counts** word frequency using pandas (`value_counts()`)
5. **Exports** the results to `MLKJ_speech_count.csv`

## Tools Used
- **Python**: `requests`, `BeautifulSoup` (web scraping), `re` (regular expressions), `pandas` (data processing/export)

## Key Insights
- The speech contains **323 unique words** across **882 total words**.
- The most frequent words are common English function words ("the" — 54 times, "of" — 49, "to" — 29, "and" — 27), as expected for any English text.
- Beyond common words, the most repeated *meaningful* words directly reflect the speech's central themes: **"freedom"** (13 occurrences), **"dream"** (11), and **"ring"** (12) — the latter from the famous repeated phrase "let freedom ring." This kind of frequency analysis is a simple but effective way to surface the core message of a text purely from word counts, without reading it.

## How to Use
1. Open `MLK_Speech_Word_Frequency_Analysis.ipynb` in Jupyter
2. Run all cells — this will scrape the speech, process it, and generate `MLKJ_speech_count.csv`
3. The output CSV is also included in this repo for reference
