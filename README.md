# Email-Monitoring-System
# Email Classification Project: Spam and Phishing Detection

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

```mermaid
graph TD;
    A[Email Data] --> B[Text Preprocessing];
    B --> C[Exploratory Data Analysis];
    C --> D[Topic Modeling];
    D --> E[Modeling];
    E --> F[Model Evaluation];
