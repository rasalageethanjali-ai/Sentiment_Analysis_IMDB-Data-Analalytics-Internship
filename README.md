**Author:** Rasala Geethanjali  
**Internship:** Cyrostack IT Solutions — Data Analytics  
**Task 3:** Sentiment Analysis using TextBlob  

---

## **Table of Contents**
1. [Project Overview](#project-overview)  
2. [Dataset](#dataset)  
3. [Technologies Used](#technologies-used)  
4. [Project Workflow](#project-workflow)  
    - Data Cleaning & Preprocessing  
    - Exploratory Data Analysis (EDA)  
    - Model Implementation  
5. [Results](#results)  
6. [Files in Repository](#files-in-repository)  
7. [How to Run](#how-to-run)  
8. [Saving Outputs](#saving-outputs)  
9. [References](#references)  
10. [License & Disclaimer](#license--disclaimer)  

---

## **Project Overview**
This project performs **sentiment analysis** on IMDb movie reviews and classifies them as **positive** or **negative**.  
It compares traditional ML methods (**TF-IDF + Logistic Regression**) with **Transformer-based models (BERT)** to analyze sentiment with high accuracy.

---

## **Dataset**
- IMDb Reviews Dataset  
- Total Samples: 50,000  
- Source: Public IMDb dataset  

---

## **Technologies Used**
- Python 3.12  
- NLTK & TextBlob for NLP preprocessing  
- scikit-learn for TF-IDF & Logistic Regression  
- Hugging Face Transformers (BERT)  
- PyTorch for model training  
- Jupyter Notebook for development & visualization  
- Matplotlib & Seaborn for plotting  

---

## **Project Workflow**

### **1. Data Cleaning & Preprocessing**
- Removed HTML tags, special characters, and punctuation  
- Converted text to lowercase  
- Tokenized text, removed stopwords, and lemmatized  

### **2. Exploratory Data Analysis (EDA)**
- Visualized distribution of positive and negative reviews  
- Analyzed **polarity** and **subjectivity** using TextBlob  

### **3. Model Implementation**

#### **TF-IDF + Logistic Regression**
- Converted reviews to TF-IDF vectors  
- Trained a Logistic Regression classifier  
- **Accuracy:** ~88–90%  
- Generated confusion matrix & classification report  

#### **BERT Transformer Model**
- Used `bert-base-uncased` from Hugging Face  
- Tokenized reviews and fine-tuned using Hugging Face Trainer API  
- **Confidence on test samples:** 95–99%  
- Recommended: GPU for faster training  

---

## **Results**

| Model | Accuracy / Confidence |
|-------|--------------------|
| TF-IDF + Logistic Regression | 88–90% |
| BERT Transformer | 95–99% |

- **Observations:**  
  - Logistic Regression: Fast, interpretable, good baseline  
  - BERT: Context-aware, handles nuanced sentiment effectively  

---

## **Files in Repository**

| File / Folder | Description |
|---------------|-------------|
| `Sentiment_Analysis_IMDB.ipynb` | Main Jupyter Notebook with full workflow |
| `IMDb_Cleaned_Reviews.csv` | Cleaned dataset |
| `logistic_regression_model.pkl` | Saved Logistic Regression model |
| `tfidf_vectorizer.pkl` | Saved TF-IDF vectorizer |
| `bert_model/` | Folder containing saved BERT model & tokenizer |
| `requirements.txt` | Python dependencies for running the notebook |
| `README.md` | Project summary, instructions, and references |

---

## **How to Run**

1. Clone or download the repository:

```bash
git clone https://github.com/<your-username>/Sentiment_Analysis_IMDB.git
Install dependencies:

bash
Copy code
pip install -r requirements.txt
Open Sentiment_Analysis_IMDB.ipynb in Jupyter Notebook.

Run cells sequentially to reproduce:

Data cleaning & preprocessing

EDA & visualizations

Model training & evaluation

Saving Outputs
The notebook saves the following files for easy reuse and inference:

Cleaned dataset: IMDb_Cleaned_Reviews.csv

Logistic Regression model: logistic_regression_model.pkl

TF-IDF vectorizer: tfidf_vectorizer.pkl

BERT model: bert_model/ folder

References
TextBlob Documentation

NLTK Documentation

Hugging Face Transformers

FinGPT GitHub

License & Disclaimer
License: MIT License

Disclaimer: For academic purposes only. Not financial advice.
