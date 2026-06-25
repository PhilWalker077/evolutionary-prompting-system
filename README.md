# Evolutionary Prompting System (EPS) for Robust Entity Resolution

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/PhilWalker077/evolutionary-prompting-system/blob/main/Evolutionary_Prompting.ipynb)

## Overview & Description
This repository contains the final project developed for the COMM070 Data Science module. The primary objective of this research was to design and implement an **Evolutionary Prompting System (EPS)** using Genetic Algorithms to automatically optimize Large Language Model (LLM) prompts for Entity Resolution on unstructured, noisy datasets. 

**Development & Execution Notice:** 
The entire codebase was built, tested, and executed seamlessly within **Google Colab**. To maintain security and follow industry best practices, the private API credential has been completely removed from the code. In the configuration section of the script, you will find the placeholder line:
`os.environ["OPENAI_API_KEY"] = "use your own api key"`

To run or test this project yourself, simply open the notebook in Google Colab and replace `"use your own api key"` with your active, personal OpenAI API key.

* **Full Project Report:** [Read the detailed PDF report here](COMM070%20Data%20Science%20-%206902109(Final2).pdf)

---

## Key Visual / Performance
![Evolutionary Optimization of Prompts](image_13f12b.png)
*(Caption: The trajectory of evolutionary optimization over 8 generations, showing the Genetic Algorithm rapidly converging on high-performing prompts by Generation 4.)*

---

## Technologies Used
* **Languages:** Python 3.12
* **Libraries:** RapidFuzz (for fuzzy matching metrics)
* **Tools & Cloud Platforms:** Google Colab (Development Environment), OpenAI API (GPT-3.5-Turbo, GPT-4o)
* **Methodologies:** Genetic Algorithms (GA), CRISP-DM Data Science Framework, Automatic Prompt Engineering (APE)

---

## Methodology
1. **Data Augmentation (Hard Mode Benchmark):** Utilized the Fodor's-Zagat restaurant dataset and built a custom Python pipeline to inject synthetic noise (OCR artifacts, typographical errors, and case inconsistencies) to simulate real-world "dirty" enterprise data, expanding the corpus to 560 unique test cases.
2. **Evolutionary Algorithm Development:** Developed a system employing Direct Semantic Encoding where natural-language prompts act as evolving genotypes. Utilized a Teacher-Student architecture where GPT-4o acted as a mutation operator to iteratively refine prompts for GPT-3.5-Turbo.
3. **Benchmarking:** Evaluated the evolved prompts against industry-standard Zero-Shot and Chain-of-Thought (CoT) reasoning baselines using fuzzy matching fitness functions.
---

## Key Results & Business Impact
* **Superior Accuracy:** The Evolutionary System achieved a **70.00% accuracy**, significantly outperforming the standard Zero-Shot baseline (64.00%).
* **Critical Finding on AI Reasoning:** Revealed a catastrophic failure in the Chain-of-Thought (CoT) baseline, which plummeted to **0.00% accuracy**.
*  Qualitative analysis proved that forcing LLMs to "reason" on garbage data causes hallucinated verbosity and output schema violations.
* **Real-world Application:** This project offers a practical, low-code automated ETL framework that allows data pipelines to "self-correct" and adapt to novel noise patterns without human intervention, significantly reducing operational costs in data quality management.

---

## Repository Structure
* `COMM070 Data Science - 6902109(Final2).pdf`: Comprehensive final dissertation detailing the theoretical framework, experimental design, and empirical results.
* `image_13f12b.png`: Graph visualizing the average and best prompt accuracy across the evolutionary generations.
* `[Your_Notebook_Name].ipynb`: Python notebook containing code for data corruption, baseline evaluations, and genetic algorithm loops.
