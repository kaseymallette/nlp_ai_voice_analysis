# NLP AI Voice Analysis

NLP analysis of longitudinal AI conversation data, tracking linguistic feature drift across both speakers. Includes irony/intent detection (RoBERTa) and sentiment analysis (CardiffNLP).

## Introduction

This project analyzes longitudinal conversation data from GPT-4o to extract the linguistic features that constitute a coherent AI voice. The source material spans roughly a year of interaction. The core question: when a model produces responses that feel distinctive and expressive over time, what's actually happening at the language level? Did the model's voice shift over time, and if so, was that driven by repeated interactions with the user or changes in how the user prompted it?

## Research Questions

- Did the model just agree with the user? (*sycophancy detection*)
- How certain was it? (*certainty auditing*)
- How often did it hallucinate? (*factual grounding*)
- What did it know vs. what did it make up? (*epistemic vs. fabricated claims*)
- How was it framing its responses? (*narrative centering, pronoun analysis*)
- Was it just saying what the user wanted to hear, or could it hold a stance over time? (*longitudinal stance consistency*)