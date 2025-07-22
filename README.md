# 📱 SMS Spam Classifier

📎 **Project Report Link**: [View on Google Drive](https://drive.google.com/file/d/1oeY9YmHVz6AMXgAnR0jYAXZfdC6mrX_j/view?usp=drivesdk)

## 📘 Overview

This project is a **Machine Learning-based SMS Spam Classifier** that classifies SMS messages as **spam** or **ham** using various supervised learning techniques. The goal is to build an efficient and accurate classifier capable of minimizing false positives and negatives while improving user privacy and message security.

Developed as a **Data Mining for Knowledge Discovery Project (Semester V)** by:
- Kusum (22/25002)
- Aditya Kumar (22/25012)
- Divyanshi (22/25021)
- Tushar Rana (22/25064)

**Supervisor**: Mr. Mahesh Kumar  
**Institution**: Atma Ram Sanatan Dharma College, University of Delhi

---

## 📊 Dataset Description

- 📌 **Source**: [SMS Spam Collection Dataset - Kaggle](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset)
- 📈 **Total Records**: 5,572
- 🧮 **Attributes**:
  | Column Name   | Description              | Type    |
  |---------------|--------------------------|---------|
  | V1            | Target (ham/spam)        | Nominal |
  | V2            | Message Text             | Nominal |
  | Unnamed: 2    | Mostly Null              | Nominal |
  | Unnamed: 3    | Mostly Null              | Nominal |
  | Unnamed: 4    | Mostly Null              | Nominal |

- 📉 **Missing Values**: Unnamed columns have >50% nulls and are dropped
- 🔍 **Features Created**:
  - `num_characters`: Character count
  - `num_words`: Word count
  - `num_sentences`: Sentence count
  - `transformed_text`: Cleaned and preprocessed text (lowercasing, stemming, punctuation removal, etc.)

---

## 🛠️ Data Preprocessing

- Handling Null & Duplicate Values
- Feature Extraction and Engineering
- Feature Scaling (Normalization & Standardization)
- Label Encoding (ham → 0, spam → 1)
- Train-Test Splitting using:
  - Hold-out Method
  - Random Subsampling
  - K-Fold Cross-Validation

---

## 🤖 Models Used

### 1. K-Nearest Neighbour (KNN)
- Distance: Euclidean
- Lazy learning algorithm
- Tested under various split techniques

### 2. Naive Bayes
- Probabilistic classifier using Bayes Theorem
- Assumes feature independence
- Highest observed accuracy: **96.13%**

### 3. Decision Tree
- Uses attribute-based splits
- Interpretable model with pruning
- Good performance, especially with cross-validation

---

## 📈 Model Evaluation

### Evaluation Metrics:
- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

### Summary Table (Highest Scores Observed):
| Model        | Split Type    | Accuracy | Precision | Recall  | F1 Score |
|--------------|---------------|----------|-----------|---------|----------|
| Naive Bayes  | Hold-out (0.2)| **0.961** | 0.962     | **0.961** | 0.958    |
| KNN          | Hold-out (0.2)| 0.896    | 0.907     | 0.896   | 0.869    |
| Decision Tree| CV (0.2)      | 0.937    | 0.934     | 0.937   | 0.932    |

---

## ✅ Inference

- **Naive Bayes** proved to be the most effective model for this dataset with the highest accuracy and recall.
- **Cross-Validation** provides more stable results over hold-out in most cases.
- Outliers were **not removed**, considering they might represent rare but legitimate or malicious messages.

---

## 🧠 Future Enhancements

- Integration of **NLP techniques** like TF-IDF, N-Grams, or Word Embeddings.
- Deployment via Flask/Streamlit for real-time spam detection.
- Larger and more diverse SMS datasets.

---

