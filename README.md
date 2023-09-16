# Tweet-Sentiment-Extraction

The objective is to construct a model that can look at the labeled sentiment for a given tweet and figure out what word or phrase best supports it.

# The Metric Demystified: Jaccard Score
The metric in this competition is the word-level Jaccard score. Jaccard Score is a measure of how similar/dissimilar two sets are. 
The higher the score, the more similar the two strings. The idea is to find the number of common tokens and divide it by the total number of unique tokens. 
Its expressed in the mathematical terms by

<p align="center">
![lMHa8CL](https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/40a5a93c-a06e-4ab5-9a74-ecb8491de068)
</p>

<p align="center">
![jaccard-index-391304](https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/be36bfba-bc1e-4767-9a91-a56ab637ff99)
</p>


Here is a great example to understand the Jaccard Similarity Metric in an inutitve way.

<p align="center">
![ezgif-3-ec7ab86440](https://github.com/UKVeteran/Tweet-Sentiment-Extraction/assets/39216339/1dc4c0e5-0330-4728-8e2e-bfd7fb867fb5)
</p>
