# Real-Time Sentiment Analysis of Nigerian Tweets

**Status:** Archived | **Type:** Final Year Project (BSc Computer Science)  
**Date:** April 2021 | **Institution:** Loughborough University

A completed academic project exploring real-time sentiment analysis of Nigerian Twitter data using Python, NLP techniques, and visual analytics. Originally deployed as a public-facing dashboard (Heroku deployment now offline).

---

## Project Summary

This project investigates how public sentiment towards Nigerian musicians can be quantified and tracked using Twitter. It builds a lightweight data pipeline for:

- **Live tweet extraction**
- **Text pre-processing**
- **Sentiment scoring** via TextBlob
- **Storage** in PostgreSQL
- **Interactive dashboard visualisation** using Dash & Plotly

The system monitored mentions of popular Nigerian artists, assigned polarity scores to tweets, and visualised the evolving public opinion in real time.

---

## Tech Stack

- **Language**: Python 3.8
- **Libraries**: Tweepy, TextBlob, NLTK, pandas, Dash, Plotly, WordCloud, SQLAlchemy
- **Database**: PostgreSQL
- **Deployment (archived)**: Heroku (Dyno + Scheduler)

---

## System Architecture

```text
           ┌────────────┐
           │ Twitter API│
           └────┬───────┘
                │
        ┌───────▼────────┐
        │ Text Cleaning  │  ← remove links, mentions, emojis, casing, etc.
        └───────┬────────┘
                │
        ┌───────▼────────┐
        │ Sentiment Scoring │ ← TextBlob polarity (-1 to 1)
        └───────┬────────┘
                │
        ┌───────▼────────┐
        │ PostgreSQL DB  │ ← Store processed tweets + scores
        └───────┬────────┘
                │
        ┌───────▼────────┐
        │ Dash Dashboard │ ← Charts, tables, word clouds
        └────────────────┘
```

---

## Output Highlights

* Area graph of positive/neutral/negative sentiment over time
* Ranking of musicians by average sentiment score
* Pie chart sentiment distribution
* Word cloud of most frequent tweet terms

---

## Project Files

* `clock.py` – Scheduled tweet extractor
* `app.py` – Dash dashboard application
* `requirements.txt` – Python dependencies
* `Procfile`, `runtime.txt` – Heroku deployment config
* `musicians.txt` – Search terms for tweet collection

---

## Note on Deployment

The public dashboard (originally hosted on Heroku) is no longer active due to decommissioned dyno services. The codebase remains available for review, adaptation, or redeployment.
