
# NLP
This Repo contains some of my notes in relation to Natural Language Processing (NLP). I will try to update it as I proceed with my NLP journey.

### Requirments
The requirements and Library used can be found in [requirements.txt](https://github.com/Azizkhaled/NLP-with-Aziz/blob/main/requirements.txt). Hopefully, all notebooks can be run on Google Colab with no problems. 

## Contents
### 1. Pre-processing Techniques
I will share some common techniques used for NLP pre-processing in the 
[NLP_Preprocessing.ipynb](https://github.com/Azizkhaled/NLP-with-Aziz/blob/main/NLP_Preprocessing.ipynb)
          
        -  Removing Stopwords
        -  Tokens
        -  Stemming
        -  Lemmatization
        -  Unicode Normalization
    

### 2. Attention
Common Attention mechanisms in relation to NLP can be found in [NLP_Attention.ipynb](https://github.com/Azizkhaled/NLP-with-Aziz/blob/main/NLP_Attention.ipynb)

        - Encoder-Decoder Attention (Dot-Product Attention)
        - Self Attention
        - Bidirectional Attention
        - Multi-head Attentenion

### 3. Language Classifications
Some Sentiment classification techniques are explored in this notebook. [NLP_Language_Classification_Flair_Transformers](https://github.com/Azizkhaled/NLP-with-Aziz/blob/main/NLP_Language_Classification_Flair_Transformers.ipynb)
        
        - Sentiment Classification with flair
        - Sentiment Classification with Transformers

### 4. Long Text Classification
Similar to 3, but here we explore other techniques if the sample size is bigger than the transformer capabilities [Long_text_classification.ipynb](https://github.com/Azizkhaled/NLP-with-Aziz/blob/main/Long_text_classification.ipynb)
        
        - Bert issue
        - Long text solution: Window Partitioning
        - Applying window method using Pytorch

### 5. Named Entity Recognition
Here, we discover how to perform Entity Recognition with Spacy, and how to extract a single entity of interest. [NER.ipynb](https://github.com/Azizkhaled/NLP-with-Aziz/blob/main/NER.ipynb)
We also go through the steps of pulling data from subreddits using Praw, and extracting the organization entities from the top 100 hottest posts in the r\investing subreddits [NER_On_Sub_reddits.ipynb](https://github.com/Azizkhaled/NLP-with-Aziz/blob/main/NER_On_Sub_reddits.ipynb)
        
        - Download NER model
        - Extract Entity
        - Pulling Data from Reddit
        - Extract ORGs from data
        - Function to get the most mentioned ORG


  

## NLP Projects: 
### 1. Movie Reviews Classification
In this project we use the Rotten Tomatoes dataset from Kaggle. We try to classify it into one of 5 classes; (negative, somewhat negative, neutral, somewhat positive, and positive). 
We fine-tune the Bert pre-trained model 
[Movie_Reviews_Classification_with_TF.ipynb](https://github.com/Azizkhaled/NLP-with-Aziz/blob/main/Movie_Reviews_Classification_with_TF.ipynb)

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



  
