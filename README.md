# Prompt Engineering Lab

## Overview
This lab explores the empirical side of prompt engineering by building production-ready prompts through systematic testing, iteration, and refinement.

It documents the process of taking unstable zero-shot prompts and iteratively upgrading them using Few-Shot Prompting and Chain-of-Thought (CoT) Reasoning to achieve output consistency across repeated stress tests.

## Key Results

| Task | v1(zero-shot) | v3(tuned) |
|---|---|---|
| Sentiment classification | 43% consistency | 93% consistency |
| Data Extraction | 14% consistency | 100% consistency, 100% valid JSON |
| Product Description | 0% text consistency | Structure locked 100%, hallucination eliminated |

## What it includes
1. **Jupyter Notebook** - `prompt_engineering_lab.ipynb` the full lab, covering three tasks (sentiment analysis, product description generation, data extraction), each carried through v1 (zero-shot), v2, and v3 (few-shot / chain-of-thought) prompt versions. Includes 5/10/15-run consistency testing for each version, task-variation stress tests, and a final comparison report.
2. **Lab Summary** - `lab_summary.md`  a short summary of what was done and the key lessons learned.