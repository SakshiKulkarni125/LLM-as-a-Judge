# LLM-as-Judge Evaluation Project

## Overview

This project implements an **LLM-as-Judge evaluation pipeline**, where one Large Language Model (LLM) generates responses and another LLM evaluates the quality of those responses.

The system uses a golden dataset containing questions and expected answers, generates responses using a generator LLM, and evaluates them using a judge LLM across multiple quality metrics. The final evaluation results are stored in a CSV file for analysis.

---

## Project Structure

```text
.
├── README.md
├── requirements.txt
├── data/
│   ├── goldendataset.json
│   └── evaluation_results.csv
├── prompts/
│   ├── generator_prompt.txt
│   └── judge_prompt.txt
└── src/
    ├── main.py
    ├── evaluator.py
    ├── generator_llm.py
    ├── judge_llm.py
    └── generate_dataset.py
```
## Project Workflow

### 1. Golden Dataset
A dataset of:
- Questions
- Expected (golden) answers

is used as the benchmark for evaluation.

### 2. Generator LLM
The generator model produces answers for each question in the dataset.

### 3. Judge LLM
The judge model compares:
- Generated answers
- Golden answers

and assigns evaluation scores.

### 4. Evaluation Metrics
The generated responses are evaluated on:
- Correctness
- Relevance
- Completeness
- Faithfulness
- Hallucination
- Reasoning Quality
- Fluency and Readability
- Coherence
- Semantic Similarity
- Safety and Toxicity

### 5. Result Storage
All evaluation results are saved into a CSV file for further analysis and comparison.

---

## Features

- Automated LLM answer generation
- LLM-based evaluation pipeline
- Multi-metric scoring system
- CSV result export
- Structured and reusable dataset format
- Easy experimentation with prompts and models

---

## Tech Stack

- Python
- Pandas
- OpenAI API / LLM APIs
- CSV for dataset and output handling

---
