# Leveraging LLMs to Extract Cancer Patient Experiences

## Overview
This repository contains code and resources for leveraging Large Language Models (LLMs) to extract cancer patient experiences from online narratives, particularly Reddit posts. The project focuses on zero-shot prompt engineering to analyse patient-generated content and identify themes, values, preferences, and concerns.

## Introduction
Social media platforms have become a vital resource for healthcare research, as patients and caregivers increasingly turn to the web for information and support. Platforms like Reddit host diverse cancer-related communities where users share unedited thoughts, experiences, concerns, and sentiments. These narratives are rich in information but are typically unstructured, making them challenging to analyze.

Large Language Models (LLMs) offer a promising solution by extracting structured insights from unstructured text. Using carefully designed prompts, LLMs can identify important aspects of patient experiences, including:

- **Themes:** Symptoms, treatment encounters, emotional reactions, coping strategies, social support, and interactions with healthcare professionals.  
- **Values:** Beliefs, principles, or priorities that influence decision-making.  
- **Preferences:** Subjective choices or desires regarding medical care and treatment options.  
- **Concerns:** Specific issues, worries, or priorities expressed by patients.

This project employs zero-shot prompt engineering to maximize LLMs’ capabilities without requiring labeled data.

## Methods and Data
- **LLMs Used:** GPT-3.5, ChatGLM3, Llama2  
- **Dataset:** 2000 patient narratives from Reddit covering breast, prostate, and melanoma cancers  
- **Approach:** Zero-shot prompt engineering with two types of templates:
  1. **Basic Prompt (Pbasic):** `TextData + PQues + OutputConstraint`  
  2. **Augmented Prompt (Paug):** `TextData + PContext + PQues + OutputConstraint`  

Where:  
- `TextData`: Online post by a cancer patient  
- `PQues`: The question/task for the LLM  
- `PContext`: Additional context to enhance LLM comprehension  
- `OutputConstraint`: Format restrictions on the output

The goal is to extract structured insights directly from unstructured narratives.

## Results
- Zero-shot prompting produced promising results for cancer-specific data.  
- Human annotators evaluated LLM outputs based on:
  1. **Fluency** – Smoothness and readability  
  2. **Relevance** – Alignment with prompt or context  
  3. **Coherence** – Logical and cohesive narrative  
  4. **Grammatical Correctness** – Accuracy of language  
  5. **Diversity** – Variation of outputs across prompts  
- Augmented prompts improved understanding and accuracy compared to basic prompts.

## Conclusion
This study demonstrates that LLMs, guided by zero-shot prompt engineering, can effectively extract themes, values, preferences, and concerns from unstructured patient narratives. Contextually enhanced prompts improve comprehension and produce more accurate and actionable insights.

