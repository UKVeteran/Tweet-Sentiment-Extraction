# Tweet-Sentiment-Extraction

<a href="https://www.kaggle.com/competitions/tweet-sentiment-extraction/">Kaggle Tweet Sentiment Extraction Dataset</a>

The objective is to construct a model that can look at the labeled sentiment for a given tweet and figure out what word or phrase best supports it.



# The Metric Demystified: Jaccard Score
The metric in this competition is the word-level Jaccard score. Jaccard Score is a measure of how similar/dissimilar two sets are. 
The higher the score, the more similar the two strings. The idea is to find the number of common tokens and divide it by the total number of unique tokens. 
Its expressed in the mathematical terms by

<p align="center">
   <img width="600" src="https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/40a5a93c-a06e-4ab5-9a74-ecb8491de068" alt="">
</p>


<p align="center">
     <img width="600" src="https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/be36bfba-bc1e-4767-9a91-a56ab637ff99" alt="">
</p>


Here is a great example to understand the Jaccard Metric in an inutitve way:

<p align="center">
     <img width="600" src="https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/9dedaf72-ed8e-468f-b8f0-be5736c4092d" alt="">
</p>


<p align="center">
     <img width="600" src="https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/f40c9035-8b4e-4a7c-9130-27b5ccd55303" alt="">
</p>

## Sources
1) <a href="https://en.wikipedia.org/wiki/Jaccard_index" >Wikipedia Article </a><br>
2) <a href="https://dataaspirant.com/five-most-popular-similarity-measures-implementation-in-python" >DataAspirant Article</a>

# Data Viz.

## Wordcloud
<p align="center">
     <img width="12000" src="https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/97270ed8-05c8-4dae-90b9-a8bc90e1c0db" alt="">
</p>

## Text Length Distribution
### Positive
![positive](https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/d076084b-b982-4a37-b760-bcf4d3a4d900)

### Neutral
![neutral](https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/73f823c6-cf02-40aa-a10b-a3e28fcd26e8)

### Negative
![negative](https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/bcffac63-2091-4c5c-bc33-0a2f77f419e9)

## Length of Text
![lengthoftext](https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/6aa103f7-2b2f-4884-af74-c1c70439edfb)


## Text Word Count
### Positive
![positive](https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/f9a899af-4b34-47eb-a7f8-ecef07893433)

### Neutral

![neutral](https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/4e1ab969-97eb-4833-8f07-8613d1c42eec)

### Negative

![negative](https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/ace49567-d9ec-4bb1-bd99-2b3c8c929709)

## Unigrams
### Positive
![positive](https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/596cbf28-ec23-4b99-a9a6-09f7fa7595e7)

### Neutal
![neutral](https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/89cf66ef-f909-4dad-861c-a86cb57916f9)

### Negative

![negative](https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/74eade48-09e0-49df-bef7-f2a07281c0df)


## Bigrams
### Positive
![positive](https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/de16417d-05db-4e11-b91e-3b6f1a5a6ca3)

### Neutal
![neutral](https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/5de5c10c-7275-47a4-b42c-dfbb204bd125)


### Negative
![negative](https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/6b7f56e8-6c97-4acb-91a3-6af6823b7720)


## Trigrams
### Positive
![positive](https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/b2b9af05-2071-4c8f-83ee-6610cfd4688b)

### Neutal
![neutral](https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/c5aa4ceb-62ec-4751-b549-42bc683470c5)


### Negative
![negative](https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/1db58d7b-5df9-4b1c-afc3-48bcedb5b46b)


## Most Common Words

### Positive
![positive](https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/5ac14dde-1ec1-4f90-a8db-3490cac2c2cf)

### Neutral
![neutral](https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/c7fdc1bf-ce97-47f3-9667-c5ab59c0af9a)

### Negative
![negative](https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/18215ebb-68a5-4841-9141-54603366b9a1)


# BERT Base

BERT is a transformers model pretrained on a large corpus of English data in a self-supervised fashion. This means it was pretrained on the raw texts only, with no humans labeling them in any way
with an automatic process to generate inputs and labels from those texts. More precisely, it was pretrained with two objectives:
1) Masked language modeling (MLM): taking a sentence, the model randomly masks 15% of the words in the input then run the entire masked sentence through the model and has to predict the masked words. This is different from traditional recurrent neural networks (RNNs) that usually see the words one after the other, or from autoregressive models like GPT which internally masks the future tokens. It allows the model to learn a bidirectional representation of the sentence.
2) Next sentence prediction (NSP): the models concatenates two masked sentences as inputs during pretraining. Sometimes they correspond to sentences that were next to each other in the original text, sometimes not. The model then has to predict if the two sentences were following each other or not.

# RoBERTa (Robustly Optimized BERT Approach) Base
RoBERTa is a transformers model pretrained on a large corpus of English data in a self-supervised fashion. This means it was pretrained on the raw texts only, with no humans labelling them in any way with
an automatic process to generate inputs and labels from those texts.

More precisely, it was pretrained with the Masked language modeling (MLM) objective. Taking a sentence, the model randomly masks 15% of the words in the input then run the entire masked sentence through the 
model and has to predict the masked words. This is different from traditional recurrent neural networks (RNNs) that usually see the words one after the other, or from autoregressive models like GPT which internally
mask the future tokens. It allows the model to learn a bidirectional representation of the sentence.

