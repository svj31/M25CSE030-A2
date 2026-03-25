# Natural Language Understanding — Assignment 2

## Overview
This repository contains solutions for Assignment 2 of the Natural Language Understanding course. The assignment consists of two main problems:

1. Word Embeddings using Word2Vec
2. Character-Level Name Generation using RNN variants

All implementations are done from scratch to understand the internal working of the models.

---

# Problem 1: Word Embeddings using Word2Vec

## Files
- `academic_1.txt` → Academic document
- `academic_2.txt` → Academic document
- `course_text.txt` → Course content
- `corpus.txt` → Combined dataset
- `prob1.ipynb` → Implementation notebook

---

## Dataset
The dataset is created using IIT Jodhpur related content:
- Website pages
- Academic regulations
- Course syllabus

---

## Preprocessing
- Lowercasing text
- Removing special characters and HTML
- Tokenization
- Stopword removal
- Filtering short sentences

---

## Models Implemented
- CBOW (Continuous Bag of Words)
- Skip-gram with Negative Sampling

---

## Key Observations
- Skip-gram performs better than CBOW
- Model captures semantic relations like:
  - student → academic, semester
  - phd → mtech, degree

---

## Visualizations
- Word Cloud
- PCA plots
- t-SNE plots

---

# Problem 2: Character-Level Name Generation

## Files
- `TrainingNames.txt` → Dataset of names
- `NLU_Assignment2_prob2.ipynb` → Implementation notebook

---

## Dataset
- 1000 Indian names
- Generated using LLM

---

## Preprocessing
- Lowercasing
- Removing unwanted characters
- Adding tokens `<SOS>` and `<EOS>`
- Creating character vocabulary
- Encoding names into sequences

---

## Models Implemented
- Vanilla RNN
- BLSTM (Bidirectional LSTM)
- RNN with Attention

---

## Evaluation Metrics

### Novelty
Measures how different generated names are from training data (using similarity-based comparison).

### Diversity
Measures uniqueness of generated names.

---

## Results

| Model | Novelty | Diversity |
|------|--------|----------|
| RNN | 0.736 | 0.591 |
| BLSTM | 0.969 | 0.979 |
| Attention | 0.681 | 0.748 |

---

## Observations
- RNN produces simple but repetitive names
- BLSTM generates diverse but sometimes noisy names
- Attention model produces more realistic names

---

## Sample Outputs

**RNN:**
- ananit, kanan, shanan

**BLSTM:**
- dhavit, pavar, oochani

**Attention:**
- kanik, shanu, anika

---

## Conclusion
- Word2Vec models successfully capture semantic relationships
- Sequence models generate realistic names
- Attention mechanism gives best performance among sequence models

---

## How to Run

### Problem 1
1. Open `prob1.ipynb`
2. Run all cells

### Problem 2
1. Open `NLU_Assignment2_prob2.ipynb`
2. Run all cells

---

## 📎 Note
This project is implemented for learning purposes and focuses on understanding core NLP concepts like word embeddings, sequence models, and attention mechanisms.