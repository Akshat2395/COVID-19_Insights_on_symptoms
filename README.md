# COVID-19_Insights_on_symptoms

## Introduction

In response to the COVID-19 pandemic, the White House and a coalition of leading research groups have prepared a dataset of open sourced research papers. This data-set is a resource of over 45,000 scholarly articles, including over 33,000 with full text, about COVID-19, SARSCoV-2, and related coronaviruses. This freely available dataset is provided to the global research community to apply recent advances in natural language processing and other AI techniques to generate new insights in support of the ongoing fight against this infectious disease. There is a growing urgency for these approaches because of the rapid acceleration in new coronavirus literature, making it difficult for the medical research community to keep up and extract insight from this growing body work.

**Objectives**

1. Implement functionality to parse natural language biomedical literature data according to given constraints and requirements.

2. Test machine learning algorithms like LDA and clustering methods in order to gain insights or answer the overarching question about the symptoms after getting infected.

3. Improve on skills and competencies required to collate and present domain specific, evidence-based insights. Particularly, in this case to gain insights and guide the fight against the COVID-19 pandemic.

4. Symptoms which we will deal - cold, fever, cough, rhinitis, bronchitis, bronchiolitis, pneumonia, diarrhea, headache, and fatigue.


## Outline
1. Data Cleaning
2. Data Visualization and Exploratory Analysis
3. Model Selection and Implementation
4. Insights

### 1. Data Cleaning

This step basically includes converting all text to lowercase, handle missing/null values, removing stop words and lemmatizing all the words. Lemmatization, unlike Stemming, reduces the inflected words properly ensuring that the root word belongs to the language.


### 2. Exploratory Analysis

* Frequency of appearance of symptoms in research papers throughout the years

<img src="https://github.com/Akshat2395/Twitter_Sentiment_Analysis_of_Canadian_Political_Landscape_2019/blob/main/images/neg_reason_count.png" width="1000" height="300">
