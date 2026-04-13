# Homework 4 - CS5760 NLP

## Student Information
Name: Sujan Akena  
Course: Natural Language Processing  
Semester: Spring 2026  
University: University of Central Missouri  

---

# Q6: Multi-Input Feedforward

### Hidden Layer
- z1 = 0.3  
- z2 = 1.1  
- h1 ≈ 0.574  
- h2 ≈ 0.750  

### Output
- y ≈ 0.50045  

### Loss
- Binary Cross-Entropy ≈ 0.6927  

---

# Q7: XOR with ReLU Network

### Outputs
- (0,0) → 0  
- (0,1) → 1  
- (1,0) → 3  
- (1,1) → 1  

### Conclusion
- The network does NOT compute XOR exactly  
- Incorrect for inputs:
  - (1,0)
  - (1,1)

---

# Q8: Decision Boundary and Misclassification

### Decision Boundary
x1 - 2x2 + 1 = 0  

### Classification
- Misclassified point: (3,2)

### Loss
- Number of mistakes = 1  

### Updated Weights (η = 0.5)
- w1 = 2.5  
- w2 = -1  
- b = 1.5  

---

# Part I: Short Answers

## Neural Networks
- Non-linear activations allow learning complex patterns.
- Deep networks learn hierarchical features.

## RNN Families
- Many-to-one → Sentiment analysis  
- Many-to-many → Translation  
- Many-to-many aligned → NER  

## Vanishing Gradient
- Gradients shrink → cannot learn long dependencies  
- LSTM/GRU solve using gating mechanisms  

## LSTM
- Forget gate removes information  
- Input gate adds new information  
- Output gate exposes relevant information  

## Self-Attention
- Q = Query, K = Key, V = Value  
- Attention = softmax(QKᵀ / √dₖ) V  
- Scaling prevents large values  

## Multi-Head Attention
- Learns multiple relationships in parallel  
- Improves representation  

## Masked Attention
- Prevents future information leakage  
- Used in decoder for sequence generation  

---

# Part II: Programming

## Q1: Character-Level RNN

### Model
- Embedding → LSTM → Linear → Softmax  

### Training
- Loss: CrossEntropyLoss  
- Optimizer: Adam  
- Epochs: 10  

### Training Output
Epoch 1: 36.79  
Epoch 10: 7.75  

### Generated Text

**Temperature = 0.7**
