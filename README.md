# evolutionary-prompting-system
Developed an Evolutionary Prompting System (EPS) using Genetic Algorithms to optimize LLM prompts for Entity Resolution on noisy datasets.
# Evolutionary Prompting System (EPS) for Robust Entity Resolution

## Overview
This repository contains the final project for the COMM070 Data Science module[cite: 2]. The primary objective of this research was to develop an Evolutionary Prompting System (EPS) that uses genetic algorithms to automatically optimize Large Language Model (LLM) prompts, providing a reliable framework for Entity Resolution on unstructured, noisy datasets[cite: 2]. 

**Full Project Report:** [Read the detailed PDF report here](COMM070%20Data%20Science%20-%206902109(Final2).pdf)

## Key Visual / Performance
![Evolutionary Optimization of Prompts]
*(Caption: The trajectory of evolutionary optimization over 8 generations, showing the Genetic Algorithm rapidly converging on high-performing prompts by Generation 4.)*

## Technologies Used
* **Languages:** Python 3.12
* **Libraries:** RapidFuzz (for fuzzy matching metrics)
* **Tools/Platforms:** OpenAI API (GPT-3.5-Turbo, GPT-4o)
* **Methodologies:** CRISP-DM Framework, Genetic Algorithms (GA), Automatic Prompt Engineering (APE)

## Methodology
1. **Data Augmentation (Hard Mode Benchmark):** Utilized the Fodor's-Zagat restaurant dataset and built a custom Python pipeline to inject synthetic noise (OCR artifacts, typographical errors, and case inconsistencies) to simulate real-world "dirty" enterprise data, resulting in 560 unique test cases.
2. **Evolutionary Algorithm Development:** Developed a system employing Direct Semantic Encoding where natural-language prompts act as evolving genotypes. Utilized a Teacher-Student architecture where GPT-4o acted as a mutation operator to iteratively refine prompts for GPT-3.5-Turbo.
3. **Benchmarking:** Evaluated the evolved prompts against industry-standard Zero-Shot and Chain-of-Thought (CoT) reasoning baselines using fuzzy matching fitness functions.

## Key Results & Business Impact
* **Superior Accuracy:** The Evolutionary System achieved a **70.00% accuracy**, significantly outperforming the standard Zero-Shot baseline (64.00%).
* **Critical Finding on AI Reasoning:** Revealed a catastrophic failure in the Chain-of-Thought (CoT) baseline, which plummeted to **0.00% accuracy**. Qualitative analysis proved that forcing LLMs to "reason" on garbage data causes hallucinated verbosity and output schema violations.
* **Real-world Application:** This project offers a practical, low-code automated ETL framework that allows data pipelines to "self-correct" and adapt to novel noise patterns without human intervention, significantly reducing operational costs in data quality management.

## Repository Structure
* `COMM070 Data Science - 6902109(Final2).pdf`: Comprehensive final dissertation detailing the theoretical framework, experimental design, and empirical results.
* `image_13f12b.png`: Graph visualizing the average and best prompt accuracy across the evolutionary generations.
