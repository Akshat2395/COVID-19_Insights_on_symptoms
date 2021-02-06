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

* Count of symptoms in all research papers

<img src="https://github.com/Akshat2395/COVID-19_Insights_on_symptoms/blob/main/images/Frequency_symptoms.png" width="1000" height="300">

The bar chart shows the frequency of our vocabulary list in all of our research papers. We can see that the word 'pneumonia' was emphasized the most followed by 'diarrhea' and then 'fever'.

* Frequency of appearance of symptoms in research papers throughout the years

<img src="https://github.com/Akshat2395/COVID-19_Insights_on_symptoms/blob/main/images/appearance_througout_years_1.png" width="1000" height="350">
<img src="https://github.com/Akshat2395/COVID-19_Insights_on_symptoms/blob/main/images/appearance_througout_years_2.png" width="1000" height="350">
<img src="https://github.com/Akshat2395/COVID-19_Insights_on_symptoms/blob/main/images/appearance_througout_years_3.png" width="1000" height="175">


### 3. Model Selection

* **Agglomerative clustering with TF-IDF**

Tf-idf stands for term frequency-inverse document frequency, and the tf-idf weight is a statistical measure used to evaluate how important a word is to a document in a collection or corpus. The importance increases proportionally to the number of times a word appears in the document but is offset by the frequency of the word in the corpus.

Agglomerative clustering is a type of Hierarchical clustering technique which follows a bottom to top approach in which clusters are made consisting of individual keywords and in the following iterations, they merge until a single parent node has been reached.

Cluster 1 represents 'fever', 'cough', 'headache' and 'fatigue'.

Cluster 2 represents 'bronchiolitis' and 'pneumonia'.

Cluster 3 represents 'rhinitis', 'bronchitis' and 'cold'.

Cluster 1 represents symptoms which occur at a very early stage of infection by a coronavirus. From various sources, we know that people diagnosed with COVID-19 had cough and fever as their initial symptoms. Elements in cluster 2 represent medical conditions which occur at a later stage where the virus starts affecting the lungs. These are 'bronchiolitis' and 'pneumonia'. Cluster 3 represents medical conditions like 'rhinitis' and 'bronchitis' which are severe conditions and patients require special care and might also require special medical equipments to help them cure.


* **Latent Dirichlet Allocation (LDA)**

We will use Latent Dirichlet Allocation (LDA) as our unsupervised model which is a topic modeling technique. It is usually used to convert a set of research papers to a set of topics. Here, we will be using our own list of dictionary, which is the list of symptoms for the coronavirus disease. These are called topics. Each document or research paper is represented as a distribution over these topics and each topic is represented as a distribution of the list of words (or topics in our case).

**Please look into the python file for the interactive LDA plot to visualize the clusters better.**


### 4. Insights

COVID-19 is one of the coronaviruses which can be transferred to humans from consumption of wild animals. As it is a novel virus, it is similar to other members of the coronavirus family like SARS and MERS. By looking at them, we found out that the symptoms of COVID-19 also coincide with the other members of its family. These symptoms are 'cold', 'fever', 'cough', 'rhinitis', 'bronchitis', 'bronchiolitis', 'pneumonia', 'diarrhea', 'headache' and 'fatigue'. Given thousands of research papers written on coronaviruses, the common thing between all of them are the symptoms. That is why I chose to go with the analysis of symptoms.

From the above 2 implemented models, Hierarchical clustering gave us promising results in terms of forming clusters with similar features. The similarity was computed by calculating a distance matrix and then a dendogram was formed which gave us a visual representation of the clusters. Clusters were formed on the basis of severity of the infection. Cluster 1 gave us symptoms which usually occur in the early stages of infection. Similarly, cluster 2 consists of symptoms which a COVID-19 patient shows at a later stage (like after 10 days). Cluster 3 consists of medical conditions which are fatal to humans and might also lead to death.

The cluster order gives us a brief insight on what stage the infected person is at and what medical needs is required either in order to cure him, or to provide medical help. These insights would have been useful if this was done at an earlier stage (let's say when this novel virus was first detected) as then, we could predict what medical supplies and medical equipments would be required to cure or help the person in need.
