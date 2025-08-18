
# Zambia Gazette Text Classification Project



## Table of Contents
1. [Business Understanding](#1-business-understanding)  
2. [Methodology](##1.8-methodology)  
3. [Tools and Technologies](##1.9-tools-and-technologies)  
4. [Expected Outcomes](##1.10-expected-outcomes)  
5. [Future Enhancements](##1.11-future-enhancements)
6. [Data Understanding](#2-data-understanding) 


# 1. BUSINESS UNDERSTANDING
## 1.1 PROBLEM STATEMENT

The Zambia Government Gazette publishes official notices, legal updates, tenders, and public announcements. These documents are published in PDF format, and often unstructured, making it difficult for stakeholders such as lawyers, journalists, researchers, and the general public to quickly find relevant information. Manual searching is time-consuming and prone to oversight. There is a need for an automated method to classify Gazette notices into categories (e.g., legal notices, tenders, appointments, public warnings) for faster retrieval and analysis.

## 1.2 BUSINESS OBJECTIVES

The primary objective is to develop a system that automatically processes and classifies Gazette publications into predefined categories. Success will mean that end users can:

Quickly identify and filter notices by category.

Reduce time spent manually scanning through documents.

Gain improved access to relevant legal or public information.

From a real-world perspective, this will increase efficiency for professionals and citizens who rely on the Gazette for important updates.

## 1.3 DATA MINING GOALS

We will build a text classification model that:

Extracts text from Gazette PDFs.

Preprocesses the text (cleaning, tokenization, stopword removal).

Classifies each notice into categories.

Outputs labeled data for easy search and retrieval.

The approach will likely involve Natural Language Processing (NLP) and machine learning algorithms such as Logistic Regression or Support Vector Machines.

## 1.4 INITIAL SUCCESS CRITERIA

The project will be considered successful if:

The classification model achieves at least 80% accuracy on the test dataset.

Categories are clearly and vividly defined, distinct, and interpretable.

The pipeline can handle at least 10 new Gazette PDFs per month without major manual intervention.

Users confirm that classification results improve search speed and relevance compared to manual reading.

## 1.5 SCOPE & ASSUMPTIONS

Scope:

Focus on classifying Gazette notices into 4–6 main categories.

Work only with English-language Gazettes.

Process and analyze a subset of recent Gazette issues.

Assumptions:

PDF files are accessible and legally permissible for analysis.

Categories remain consistent over time.

OCR (Optical Character Recognition) will be needed for scanned documents.

## 1.6 RISKS & CONSTRAINTS

Risks:

Poor text quality from scanned PDFs may reduce OCR accuracy.

Some notices may belong to multiple categories, complicating classification.

Limited labelled training data could impact model performance.

Constraints:

Legal constraint: Must comply with any copyright or government data use regulations.

## 1.7 Expected Benefits
The system will enable faster retrieval of Gazette notices, enhance transparency, and support informed decision-making for both professionals and the public.

## 1.8 METHODOLOGY
### 1.8.1 DATA COLLECTION

Download Gazette PDFs from the official Zambia Government Gazette website.

Ensure documents cover a representative period to include diverse categories.

Maintain a record of file metadata (date, publication number) for reference.
### 1.8.2 DATA PREPROCESSING

Convert PDFs to text using OCR for scanned documents.

Remove irrelevant elements (headers, footers, page numbers).

Tokenize text and remove stopwords, punctuation, and special characters.

Standardize text formatting (e.g., lowercasing, stemming).

### 1.8.3 MODEL SELECTION

Evaluate multiple classification algorithms: Logistic Regression, Support Vector Machines, and Random Forest.

Use TF-IDF or word embeddings to represent text features.

Optimize model parameters using cross-validation.

### 1.8.4 EVALUATION METRICS

Accuracy, precision, recall, and F1-score for each category.

Confusion matrix to identify misclassification trends.

User feedback on relevance and usefulness of classified notices.

## 1.9 TOOLS AND TECHNOLOGIES

Programming Languages: Python

Libraries: scikit-learn, pandas, NumPy, NLTK, spaCy, PyPDF2, Tesseract OCR

Environment: Jupyter Notebook / Python IDE

Version Control: Git / GitHub

## 1.10 EXPECTED OUTCOMES

Automated classification of Gazette notices into predefined categories.

A searchable dataset with labeled notices for faster retrieval.

Insights into the distribution and frequency of notice types.

Reduced manual effort for users accessing Gazette information.

## 1.11 FUTURE ENHANCEMENTS

Implement a web interface for searching and filtering classified notices.

Incorporate advanced NLP techniques like BERT for improved classification accuracy.

Expand to multilingual Gazettes or other official publications.

Introduce trend analysis and reporting for frequently published notice types.


# 2. Data Understanding

## 2.1 Loading the Dataset
( Loading CSV into Pandas DataFrame.)

## 2.2 Initial Exploration
- `df.shape`, `df.head()` and explain results.  
- `df.info()`, `df.describe(include="all")` and explain results.  

## 2.3 Visual Exploration
- Create histograms for numerical columns.  
- Create bar plots for categorical columns. 

## 2.4 Summary of Findings
- From our initial exploration of the dataset, we observed that the numerical variables have different types of distributions. Some columns appear to be fairly normally distributed, while others are highly skewed with the presence of potential outliers. We also noted that a few columns contain missing values, which will require handling in the data preparation stage. These observations suggest that transformations such as normalization, as well as careful treatment of outliers and missing data, may be necessary before further analysis..

