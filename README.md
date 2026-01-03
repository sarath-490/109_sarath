📩 SMS Spam Filter (Telco Messaging)

📌 Problem Statement

Unwanted SMS spam messages such as promotional offers, phishing attempts, and fraudulent alerts are a major concern in telecom messaging systems. These messages not only degrade user experience but also pose security and financial risks.
The objective of this project is to build an automated SMS Spam Filtering system that accurately classifies incoming SMS messages as Spam or Ham (Legitimate) using Natural Language Processing (NLP) and Machine Learning techniques.

📂 Dataset

Dataset Name: SMS Spam Collection Dataset

Source: Kaggle (Public Dataset)

Link: https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset

Dataset Description

The dataset contains a collection of SMS messages labeled as:

spam – Unwanted or malicious messages

ham – Legitimate messages

Fields:

label – spam / ham

message – raw SMS text

🧠 Solution Design & Architecture

The system follows a hybrid ML-based architecture combining statistical learning with lightweight rule-based heuristics.

1. Text Preprocessing

Lowercasing text

Removing punctuation and special characters

Tokenization

Optional stopword removal

2. Feature Engineering

TF-IDF (Term Frequency–Inverse Document Frequency) is used to convert SMS text into numerical feature vectors.

This approach captures important keywords while reducing the impact of common words.

3. Machine Learning Model

Multinomial Naive Bayes classifier is used due to its efficiency and strong performance on text classification tasks.

The model is trained on labeled SMS data and evaluated on unseen messages.

4. Rule-Based Enhancement

To improve real-world detection, a simple rule layer flags messages containing:

URLs (http, https, www)

Common spam keywords (win, free, offer, prize, claim)

This hybrid approach improves recall for promotional and phishing messages.

5. Evaluation Metrics

Accuracy

Precision

Recall

Confusion Matrix

⚙️ Tech Stack

Programming Language: Python

Libraries:

Pandas

scikit-learn

NumPy

Regular Expressions (re)

📊 Output

Classified SMS messages as Spam / Ham

Exported prediction results in CSV format

Evaluation metrics printed in notebook
