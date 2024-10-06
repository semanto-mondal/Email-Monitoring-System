# Email-Monitoring-System
# Email Monitoring System: To Understand the latent features of good and bad emails. 

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


