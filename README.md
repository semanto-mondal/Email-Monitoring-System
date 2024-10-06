# Email-Monitoring-System
# Email Monitoring System: To Understand the latent features of good and bad emails. 
## Project Demo

You can also download the email classification system APK file by visiting the following link and can install and use on your local machine:

[Email Classification System](https://email-system-kappa.vercel.app/)
 

## Problem Statement

In today's digital world, it is becoming increasingly difficult to differentiate between real and fake content. With the advancement of technology, people are more accustomed to using digital devices. However, along with the increased use of technology, the security risks are also rising tremendously.

Every day, we receive hundreds of emails in our inboxes. Most of these emails are not important—some may even contain malicious content or spam. The goal of this project is to develop several machine learning models that can classify emails as either good (legitimate) emails or bad (spam or phishing) emails.

An email contains multiple features, such as the sender, recipient, subject, body, reply-to, mime-version, SPF, DKIM signature, x-spam-status, domain name, and many others. However, it is not feasible for the general public to manually check all these fields to determine whether an email is spam or not. Therefore, this project focuses on analyzing only the email subject and body to classify emails by leveraging the power of natural language processing (NLP) and machine learning.

## Introduction

This project uses a dataset containing a variety of spam, phishing, and legitimate (good) emails. The objective is to understand the differences and common characteristics between spam and phishing emails.

### Spam vs. Phishing Emails

- **Spam Emails:** Spam refers to unsolicited, bulk emails sent to a large number of recipients for advertising, scams, or promotions. The main purpose of spam is to promote products, services, or websites. Spam emails often include marketing content, advertisements, or links to dubious websites.
- **Phishing Emails:** Phishing is a form of online scam designed to trick recipients into revealing sensitive information, such as passwords, credit card numbers, or personal details. The primary purpose of phishing emails is to influence recipients into taking specific actions, such as clicking on a malicious link or providing confidential information.

Both spam and phishing emails may use email spoofing techniques to make the emails appear as if they come from a trusted source.

### Project Approach

In this project, both spam and phishing emails are categorized as bad emails, while others are categorized as good emails. The approach involves using various text analysis and statistical methods to analyze the textual data and to develop multiple models, including both interpretable and black-box models, to classify emails based on different textual features.

### Workflow

1. **Data Preprocessing:** The process begins by cleaning and preprocessing the email subject and body text.
2. **Exploratory Data Analysis (EDA):** Extensive EDA is conducted to uncover underlying features in the textual data.
3. **Topic Modeling:** Techniques such as Latent Semantic Analysis (LSA) are applied to identify latent features in the text.
4. **Modeling:** Several machine learning models are trained to classify emails as either good or bad, based on the extracted features.
5. **Model Evaluation:** The performance of different models is compared to identify the best-performing model.

The diagram below provides a high-level overview of the workflow:

![image](https://github.com/user-attachments/assets/c3493d23-4bd8-4767-b289-cc5dac5ddac8)

## Dataset Description

The dataset used for this project is a combination of two different datasets: the IWSPA-AP-2018 (International Workshop on Security and Privacy Analytics - Anti Phishing) dataset and the Enron Spam dataset. 

- **IWSPA-AP Dataset:** Contains phishing emails and authentic emails.
- **Enron Spam Dataset:** Contains spam and non-spam (legitimate) emails.

Both datasets were originally imbalanced, meaning the number of samples for different target classes varied significantly. To address this issue, we concatenated these two datasets, resulting in a more diverse and balanced dataset better suited for training our machine learning models.

### Dataset Overview

The combined dataset consists of 17,669 entries and includes three features:

| Feature Name     | Data Type | Description                            |
| ---------------- | --------- | -------------------------------------- |
| **Email Subject** | Object    | The subject of the email               |
| **Email Body**    | Object    | The body of the email                  |
| **Label**         | Integer   | The category of the email (Good or Bad) |

This dataset forms the basis for our text-based email classification models, leveraging the emails' subject and body to categorize them as either good (legitimate) or bad (spam/phishing).


## Model Performance Comparison

This section highlights the performance comparison between traditional interpretable machine learning models and advanced deep learning models, including BERT (fine-tuning), for classifying emails as good or bad.

### Interpretable Machine Learning Models

| Metric             | Decision Tree | Random Forest |
|--------------------|---------------|---------------|
| **Accuracy**        | 0.928         | 0.962         |
| **Precision**       | 0.933         | 0.964         |
| **Recall**          | 0.923         | 0.957         |
| **F-1 Score**       | 0.926         | 0.960         |
| **Type-1 Error**    | 112           | 60            |
| **Type-2 Error**    | 136           | 73            |

### Deep Learning Models

| Metric                | Bi-directional LSTM | Transformer | BERT (Fine-tuning) |
|-----------------------|---------------------|-------------|--------------------|
| **Train Accuracy**     | 0.993               | 0.981       | 0.999              |
| **Test Accuracy**      | 0.973               | 0.977       | 0.995              |
| **Validation Accuracy**| 0.975               | 0.996       | 0.986              |
| **Training Time**      | 381 Seconds         | 346 Seconds | 3494 Seconds       |

### Key Insights

- **Interpretable Models:** Random Forest showed better performance across all metrics compared to the Decision Tree model, with a notable decrease in Type-1 and Type-2 errors. This suggests that Random Forest captures patterns in the data more effectively than a single decision tree while maintaining interpretability.
- **Deep Learning Models:** BERT (fine-tuning) outperformed both Bi-directional LSTM and Transformer models in test accuracy, achieving the highest accuracy of 99.5%. However, this came at the cost of significantly longer training time (3494 seconds). On the other hand, Transformers demonstrated excellent validation accuracy and much shorter training time, indicating a strong balance between performance and computational efficiency.
- **Conclusion:** Natural Language Processing is a very powerful topic in the field of machine learning. Encoder-Decoder-based Deep Learning model with attention mechanisms has made this field more powerful. Based on the analysis it can be concluded that conventional machine learning models such as decision trees, and random forests work fine when the sentence length is comparatively small because these don’t have the self-attention or positional encoding power as a result can’t capture long-term dependency whereas model like transformer, LSTM or BERT performs file for longer text sequences due to their ability to capture long term dependency as well as capability of understanding semantic representation of the textual data. 

## WORKFLOW OF GUI
![image](https://github.com/user-attachments/assets/1a7e6d52-dfdd-443e-8df6-582ecb94f481)

##TESTING MODEL PERFORMANCE USING GUI
![image](https://github.com/user-attachments/assets/1260f21d-d577-482c-9bcc-f0866714c948)


![image](https://github.com/user-attachments/assets/85fcc069-3294-4d1f-bfe1-f85082f257cb)


## Contributors
[Rajib Chandra Ghosh](https://github.com/rajibdave00)
