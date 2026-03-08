# NLP AI Voice Analysis

NLP analysis of longitudinal AI conversation data, tracking linguistic feature drift across both speakers. Includes irony/intent detection (RoBERTa) and sentiment analysis (CardiffNLP).

## Introduction

This project analyzes longitudinal conversation data from GPT-4o to extract the linguistic features that constitute a coherent AI voice. The source material spans roughly a year of interaction. The core question: when a model produces responses that feel distinctive and expressive over time, what's actually happening at the language level? Did the model's voice shift over time, and if so, was that driven by repeated interactions with the user or changes in how the user prompted it?

## Research Questions

- Did the model just agree with the user? (*sycophancy detection*)
- How certain was it? (*certainty auditing*)
- How often did it hallucinate? (*factual grounding*)
- What did it know vs. what did it make up? (*epistemic vs. fabricated claims*)
- How was it framing its responses? (*narrative centering, hypothesis tracking*)
- Was it just saying what the user wanted to hear, or could it hold a stance over time? (*stance consistency*)

## Methodology

### Dataset

The dataset consists of conversation exports from GPT-4o, organized by month. Key conversations and moments were selected for linguistic analysis based on relevance to the research questions. Each month's data is processed through the same analysis pipeline to enable longitudinal comparison.

Raw conversation data is excluded from the public repository (`.gitignore`). 

### Libraries

**NLTK** — Descriptive statistics and exploratory analysis
- Prompt counts per month
- Word counts (user vs. AI) with min, max, median, standard deviation
- Most common words/tokens
- Conversation length distributions

**spaCy** — Dependency parsing, linguistic structure

**CardiffNLP** — Sentiment analysis

**Hugging Face** (cardiffnlp/twitter-roberta-base-irony) — Irony/intent detection

## Project Structure

```
nlp_ai_voice_analysis/
├── README.md
├── notebooks/
│   ├── 01_descriptive_stats.ipynb
│   ├── 02_sentiment_analysis.ipynb
│   ├── 03_irony_detection.ipynb
│   ├── 04_certainty_auditing.ipynb
│   └── ...
├── chats/                            # .gitignore — raw conversation exports
├── data/                             # generated datasets from analysis
└── src/                              # later, if refactored
```