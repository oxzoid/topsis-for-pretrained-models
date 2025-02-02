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

![TOPSIS Conversational Model Ranking]
Final Ranking of Text Conversational Models:
|                                  |   BLEU |   ROUGE-1 |   ROUGE-2 |   ROUGE-L |   Response Length |   TOPSIS Score |   Rank |
|----------------------------------|--------|-----------|-----------|-----------|-------------------|----------------|--------|
| microsoft/DialoGPT-small         |      0 |  0.884615 | 0.870707  |  0.884615 |               6.6 |       1        |      1 |
| google/flan-t5-small             |      0 |  0.21196  | 0.0421053 |  0.19196  |              12.6 |       0.341985 |      2 |
| facebook/blenderbot-400M-distill |      0 |  0.134559 | 0         |  0.134559 |              15.4 |       0.298268 |      3 |
| EleutherAI/gpt-neo-125M          |      0 |  0.251527 | 0.212662  |  0.251527 |              34.6 |       0.188211 |      4 |
| bigscience/bloom-560m            |      0 |  0.224029 | 0.186909  |  0.224029 |              41   |       0.132989 |      5 |

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

