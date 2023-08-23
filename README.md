
# NLP
This Repo contains some of my notes in relation to Natural Language Processing (NLP) and Transformer models. I will try to update it as I proceed with my NLP journey.

### Requirments
The requirements and Library used can be found in [requirements.txt](https://github.com/Azizkhaled/NLP-with-Aziz/blob/main/requirements.txt). Hopefully, all notebooks can be run on Google Colab with no problems. 

## Contents
### 1. [Pre-processing Techniques.ipynb](https://github.com/Azizkhaled/NLP/blob/main/NLP_Preprocessing.ipynb)
I will share some common techniques used for NLP pre-processing in the 
[NLP_Preprocessing.ipynb](https://github.com/Azizkhaled/NLP-with-Aziz/blob/main/NLP_Preprocessing.ipynb)
          
        -  Removing Stopwords
        -  Tokens
        -  Stemming
        -  Lemmatization
        -  Unicode Normalization
    

### 2. [Attention.ipynb](https://github.com/Azizkhaled/NLP/blob/main/NLP_Attention.ipynb)
Common Attention mechanisms in relation to NLP can be found in [NLP_Attention.ipynb](https://github.com/Azizkhaled/NLP-with-Aziz/blob/main/NLP_Attention.ipynb)

        - Encoder-Decoder Attention (Dot-Product Attention)
        - Self Attention
        - Bidirectional Attention
        - Multi-head Attentenion

### 3. [Language Classifications with Transformers.ipynb](https://github.com/Azizkhaled/NLP/tree/main/Text_Classification/NLP_Language_Classification_Flair_Transformers.ipynb)
Some Sentiment classification techniques are explored in this notebook. 
        
        - Sentiment Classification with flair
        - Sentiment Classification with Transformers

### 4. [Long_text_classification.ipynb](https://github.com/Azizkhaled/NLP/tree/main/Text_Classification/Long_text_classification.ipynb)
Similar to 3, but here we explore other techniques if the sample size is bigger than the transformer capabilities 
        
        - Bert issue
        - Long text solution: Window Partitioning
        - Applying window method using Pytorch

### 5. [Named Entity Recognition.ipynb](https://github.com/Azizkhaled/NLP-with-Aziz/blob/main/NER.ipynb) and [NER on Subreddits](https://github.com/Azizkhaled/NLP-with-Aziz/blob/main/NER_On_Sub_reddits.ipynb)
Here, we discover how to perform Entity Recognition with Spacy, and how to extract a single entity of interest. [NER.ipynb]
We also go through the steps of pulling data from subreddits using Praw, and extracting the organization entities from the top 100 hottest posts in the r\investing subreddits 

        - Download NER model
        - Extract Entity
        - Pulling Data from Reddit
        - Extract ORGs from data
        - Function to get the most mentioned ORG

### 6. Question Answering:

#### a. [Question Answering.ipynb](https://github.com/Azizkhaled/NLP/tree/main/Qustions%20and%20Answers%20models/Question_Answering.ipynb)
Here we use the SQuAD dataset for an Open Domain Question Answering (ODQA) application. 

          - Download and Preprocess the data 
          - Initialize the Bert Transformer model
          - Prepare the Data Pipeline
          - Make predictions
          - Evaluate with an exact match (EM)
          - Evaluate with Rouge 

#### b. [Retrievers and ElasticSearch with Haystack.ipynb](https://github.com/Azizkhaled/NLP/tree/main/Qustions%20and%20Answers%20models/Q&A_Elasticsearch_Haystack_Retrivers.ipynb) 
In this notebook, we discover how to connect to local Elasticsearch with Haystack. Whats covered:

          - Initializing the connection
          - Adding data to the cluster
          - Retrieving Data with TF-IDF
          - Remove duplicates
          - Retrieving data with BM25

#### c. [Q&A_Full_Reader_Retrieval_model](https://github.com/Azizkhaled/NLP/tree/main/Qustions%20and%20Answers%20models/Q&A_Full_Reader_Retrieval_model.ipynb) 

          - Initialize the connection with ElasticSearch
          - Dense Passage Retriever (DPR)
          - BERT Reader model
          - Reader retriever pipeline with Haystack
          - Running Queries

### 7. [Similarity Search](https://github.com/Azizkhaled/NLP_with_Aziz/blob/main/Similarity/Similarity_Search.ipynb)

          - Similarity with Transformers and Pytorch
          - Similarity with Sentence-Transformers
  

## NLP Projects: 
### 1. Movie Reviews Classification
In this project, we use the Rotten Tomatoes dataset from Kaggle. We try to classify it into one of 5 classes; (negative, somewhat negative, neutral, somewhat positive, and positive). 
We fine-tune the Bert pre-trained model 
[Movie_Reviews_Classification_with_TF.ipynb](https://github.com/Azizkhaled/NLP/tree/main/Projects/Movie%20Reviews%20Classification/Movie_Reviews_Classification_with_TF.ipynb)

  - Kaggle on Google Colab
  - Downloading the Rotten Tomatoes movie reviews dataset
  - Preprocessing the data:
    
        - Removing duplicates
        - Tokenizing
        - Bert tokenizer
        - Save the tokens
        - One hot encoding of the labels
      
  - Creating an input pipeline:
    
        - Shuffling the data and batch it
        - Split the dataset
        - Build and train the model
        - save the model
  - Make predictions

### 2. Organizational Sentiment from r\investing
In this project, we go through the top 500 posts in the r\investing, we use the flair sentiment model to classify each post, then extract the organizational entities of each post. Lastly, we get the average sentiment for each organization and rank them from most positive to negative. Data was pulled using the same method in [NER_On_Sub_reddits.ipynb](https://github.com/Azizkhaled/NLP/tree/main/Projects/Organizational%20Sentiment%20from%20r%5Cinvesting/NER_On_Sub_reddits.ipynb) 
Project : [Sentiment_of_organizations_in_Reddit.ipynb](https://github.com/Azizkhaled/NLP/tree/main/Projects/Organizational%20Sentiment%20from%20r%5Cinvesting/Sentiment_of_organizations_in_Reddit.ipynb)

### 3. Open-Domain QA Project

building an open-domain question answering system. It involves three key components: a database containing UN report data, a retriever utilizing Elasticsearch for document retrieval, and a reader utilizing the bert-base-cased-squad2 model for context comprehension. [QA_project](https://github.com/Azizkhaled/NLP_with_Aziz/blob/main/Projects/QA_with_bert%26ElasticSearch/QA_project.ipynb) 

Project Components:
  - Prepare the Database: 

        - Setting Up an Index in Elasticsearch
        - Format the Data
        - Uploading the formatted data to the Elasticsearch index.
  
  - Retriever and Reader Setup: 
       
        - BM25 retriever
        - FARMReader with the `bert-base-cased-squad2`
        - ExtractiveQAPipeline
  
  - Running Queries

### 4. Fine-Tuning BERT for Masked Language Modeling (MLM) and Next Sentence Prediction (NSP)

This project delves into the fine-tuning of a BERT language model for the tasks of MLM and NSP. Through a step-by-step approach, it explores two distinct training methods: manual PyTorch training and utilizing HuggingFace's Trainer class. [MLM_NSP_Training.ipynb](https://github.com/Azizkhaled/NLP_with_Aziz/blob/main/Projects/Training-Pretrained-Bert-Model/MLM_NSP_Training.ipynb) 

The project contains: 

        - Data loading, cleaning, and tokenization, 
        - Label tensor creation and random token masking. 
        - Label tensor creation for NSP
        - Creating a PyTorch dataset 
        - Training using manual PyTorch training
        - Training using HuggingFace's Trainer class 
        
