# TOPSIS-Based Evaluation of Conversational AI Models

## Author: Pranav Dev Khindria
**Roll Number:** 102203279

## Project Overview
This project applies the **TOPSIS (Technique for Order of Preference by Similarity to Ideal Solution)** method to evaluate different **pre-trained conversational AI models** available on Hugging Face. The models are ranked based on various performance metrics.

## Models Evaluated
- **bigscience/bloom-560m**
- **microsoft/DialoGPT-small**
- **facebook/blenderbot-400M-distill**
- **google/flan-t5-small**
- **EleutherAI/gpt-neo-125M**

## Evaluation Metrics
Each model is assessed using the following **Natural Language Processing (NLP) metrics**:
- **BLEU Score** (Measures text similarity based on n-grams)
- **ROUGE-1, ROUGE-2, ROUGE-L** (Evaluates text similarity based on recall)
- **Response Length** (A proxy for verbosity)

## TOPSIS Methodology
1. **Normalization** of evaluation metrics (to ensure comparability).
2. **Weighting of Metrics** (equal importance assumed for simplicity).
3. **Computation of Euclidean Distances** from ideal best and worst solutions.
4. **Final Ranking** using the **TOPSIS score**.

## Results
The **TOPSIS ranking** results are visualized in the following bar chart:

![TOPSIS Conversational Model Ranking](image.png)

### **Key Observations:**
- **microsoft/DialoGPT-small** achieved the highest score, indicating the best overall performance.
- Other models performed moderately well, with varying strengths across different metrics.

## How to Run the Code
### Prerequisites:
- Python 3.x
- Required libraries: `transformers`, `torch`, `pandas`, `numpy`, `sklearn`, `nltk`, `matplotlib`, `rouge-score`

### Execution Steps:
1. Install dependencies:
   ```bash
   pip install transformers torch pandas numpy scikit-learn nltk matplotlib rouge-score
   ```
2. Run the Python script:
   ```bash
   python topsis_text_conversational.py
   ```
3. View results and rankings in the terminal or generated plot.

## Conclusion
This project effectively demonstrates how **TOPSIS** can be applied to evaluate and rank conversational AI models. The ranking approach provides an **objective and quantitative assessment** of different models based on multiple evaluation criteria.

---
_Last updated: February 2025_

