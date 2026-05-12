# LLM-as-Judge Evaluation Project

## Overview

This project implements an **LLM-as-Judge evaluation pipeline**, where one Large Language Model (LLM) generates responses and another LLM evaluates the quality of those responses.

The system uses a golden dataset containing questions and expected answers, generates responses using a generator LLM, and evaluates them using a judge LLM across multiple quality metrics. The final evaluation results are stored in a CSV file for analysis.

---

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

## Project Structure

```bash
project/
│
├── dataset.csv              # Golden dataset
├── generate_answers.py      # Generates answers using LLM
├── judge_answers.py         # Evaluates generated answers
├── evaluation_results.csv   # Output evaluation file
├── requirements.txt
└── README.md
