# 📩 SMS Spam Filter (Telco Messaging)

---

## 📌 Problem Statement

Unwanted **SMS spam messages** such as promotional offers, phishing attempts, and fraudulent alerts are a major concern in modern telecom messaging systems. These messages not only **degrade user experience** but also pose **serious security and financial risks**.

The objective of this project is to build an **automated SMS Spam Filtering System** that accurately classifies incoming SMS messages as:

* **Spam** 🛑 (unwanted or malicious)
* **Ham** ✅ (legitimate messages)

This is achieved using **Natural Language Processing (NLP)** and **Machine Learning (ML)** techniques.

---

## 📂 Dataset

**Dataset Name:** SMS Spam Collection Dataset
**Source:** Kaggle (Public Dataset)
**Link:**
🔗 [https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset)

---

### 📄 Dataset Description

The dataset contains a collection of SMS messages labeled into two categories:

* **spam** – Unwanted, promotional, or fraudulent messages
* **ham** – Legitimate and safe messages

**Fields:**

| Column    | Description  |
| --------- | ------------ |
| `label`   | spam / ham   |
| `message` | Raw SMS text |

---

## 🧠 Solution Design & Architecture

The system follows a **hybrid ML-based architecture**, combining **statistical learning** with **lightweight rule-based heuristics** for improved real-world performance.

---

### 1️⃣ Text Preprocessing

To clean and normalize the SMS data, the following steps are applied:

* Convert text to lowercase
* Remove punctuation and special characters
* Tokenize the text into words
* Optional stopword removal

---

### 2️⃣ Feature Engineering

* **TF-IDF (Term Frequency–Inverse Document Frequency)** is used to convert SMS text into numerical feature vectors.
* This method:

  * Highlights important keywords
  * Reduces the impact of commonly occurring words
  * Improves classification accuracy

---

### 3️⃣ Machine Learning Model

* **Multinomial Naive Bayes Classifier** is used due to:

  * High efficiency
  * Low computational cost
  * Strong performance in text classification tasks

* The model is:

  * Trained on labeled SMS data
  * Tested on unseen messages for evaluation

---

### 4️⃣ Rule-Based Enhancement (Hybrid Approach)

To improve detection of **real-world spam**, an additional rule layer flags messages containing:

* URLs (`http`, `https`, `www`)
* Common spam keywords such as:

  * *win*
  * *free*
  * *offer*
  * *prize*
  * *claim*

📌 This hybrid approach **improves recall**, especially for promotional and phishing messages.

---

### 5️⃣ Evaluation Metrics

The system is evaluated using standard classification metrics:

* **Accuracy**
* **Precision**
* **Recall**
* **Confusion Matrix**

---

## ⚙️ Tech Stack

### 🧩 Programming Language

* **Python**

### 📚 Libraries & Tools

* **Pandas** – Data manipulation
* **scikit-learn** – Machine learning models & evaluation
* **NumPy** – Numerical computations
* **Regular Expressions (`re`)** – Text pattern matching

---

## 📊 Output

* SMS messages classified as **Spam** or **Ham**
* Prediction results exported to **CSV format**
* Evaluation metrics displayed in the notebook/console

---

## ✅ Conclusion

This project demonstrates an **efficient and scalable SMS Spam Filtering System** suitable for telecom messaging platforms. By combining **machine learning** with **rule-based heuristics**, the system achieves reliable spam detection while remaining lightweight and easy to deploy.

