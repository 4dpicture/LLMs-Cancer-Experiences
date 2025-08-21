# Metaphor-Driven Sentiment Analysis in Cancer Narratives

## Overview
This repository contains resources and analysis scripts for studying the role of metaphors in cancer narratives and their impact on sentiment interpretation. The study explores how metaphorical framing—such as "battle," "journey," and "war"—influences the emotional perception of text and how computational models and human annotators interpret these sentiments.

## Introduction
Metaphors are frequently used in oncology discourse to express personal and clinical experiences. They shape how patients communicate emotions, perceptions, and coping strategies. Understanding metaphor-driven sentiment is critical for:

- Improving human-computer interaction in healthcare applications  
- Developing empathic AI systems  
- Enhancing clinical communication  

However, interpreting metaphors is challenging due to their non-literal nature and subjective interpretations. For example, in the sentence:

> "The very best of karma, good wishes and love to you for your second battle in this bloody war"  

the sentiment is determined more by positive words like "good" and "love" than by the metaphor "battle." Changing the metaphor to "second roller coaster" alters sentiment, demonstrating the influence of metaphorical framing.

This project investigates human and machine performance in interpreting metaphorical sentiment in cancer narratives.

## Methods and Data
- **Data Source:** HealthUnlocked platform, ovarian and prostate cancer communities  
- **Dataset:**  
  - 2,624 sentences with "battle"  
  - 336 sentences with "enemy"  
  - 7,250 sentences with "fight"  
  - 7,274 sentences with "journey"  
  - 3,354 sentences with "roller coaster"  
  - 714 sentences with "war"  

- **Models Used:**  
  - **ChatGPT:** Zero-shot, prompt-based sentiment classification  
  - **RoBERTa:** Fine-tuned transformer model for sentiment detection  

- **Human Annotation:**  
  - Five annotators (native and non-native English speakers) labeled each sentence as positive, neutral, or negative  
  - Inter-annotator agreement assessed using Cohen’s Kappa on 90 randomly selected sentences (15 per metaphor)  

## Results
- **Human Agreement:**  
  - Strong agreement for "fight," "enemy," "roller coaster" (0.47–0.87)  
  - Moderate to fair agreement for "journey," "war," "battle" (0.39–0.70)  
  - Agreement varies by metaphor, reflecting subjective interpretation  

- **Model Performance:**  
  - **ChatGPT:** Moderate to strong correlation with human annotations (0.41–0.96), robust in interpreting metaphors  
  - **RoBERTa:** Poor performance on metaphor-heavy text, especially for "battle" (–0.24–0.00); fair to moderate for others (0.30–0.69)  

These results highlight the challenges of processing metaphorical language with traditional NLP models and the advantages of large generative models in understanding nuanced sentiment.

## Conclusion
Metaphor framing significantly impacts sentiment interpretation in cancer narratives. Current NLP tools struggle with affective metaphors, whereas ChatGPT demonstrates strong contextual understanding. We recommend that metaphor detection and interpretation become core tasks in NLP, particularly for emotionally sensitive domains such as healthcare.


   git clone https://github.com/yourusername/MetaphorCancerSentiment.git
