# Semantic Similarity between 2 sentences:
## Problem Statement:
Given two paragraphs, quantify the degree of similarity between the two text-based on Semantic similarity. Semantic Textual Similarity (STS) assesses the degree to which two sentences are semantically equivalent to each other. STS is the assessment of pairs of sentences according to their degree of semantic similarity. The task involves producing real-valued similarity scores for sentence pairs.
Data Description:
The data contains a pair of paragraphs. These text paragraphs are randomly sampled from a raw dataset. Each pair of the sentence may or may not be semantically similar. The candidate is to predict a value between 0-1 indicating a degree of similarity between the pair of text paras.
  - 1: Highly similar
  - 0: Highly dissimilar

## Approach:
This is a problem of Natural Language Processing (NLP) and before building any deep learning model in NLP, text embedding plays a major role. Text embedding converts text (sentences in our case) into numerical vectors.
After converting the sentences into vectors we can calculate how close these vectors are based on euclidean distance/ cosine similarity or any other method. and that itself can tell how similar our sentences are. In our case, we have used cosine similarity. 

But, how to convert keywords into vectors? we are not converting just based on keywords but the context and meaning. 
We have used Universal Sentence Encoder(USE). It encodes text into higher dimensional vectors that can be used for our semantic similarity task. The pre-trained Universal Sentence Encoder(USE) is publicly available in the TensorFlow hub.
I used USE4 because it is the state-of-the-art transformer-based model for NLP.
And is trained on a huge corpus of datasets from wikipedia.
