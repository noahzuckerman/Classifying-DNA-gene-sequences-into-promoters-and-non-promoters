# Classifying DNA sequences into Promoter and Non-promoter classes

## Executive Summary

The goal of this project is to utilize DNA text sequences (e.g. TAATAC) to build and train a machine learning model to classify whether a given DNA sequence is a promoter sequence or not.

## Problem Statement
As DNA sequence data is growing rapidly nowadays, the maintenance and annotation of these data are now of great importance. A promoter is necessary for a DNA sequence to be transcribed. With knowing the position of the promoter in the sequence, we can get the starting position of the transcription region that will later be translated into protein sequence. If we have the knowledge of which part of a DNA sequence is a promoter sequence, that promoter sequence can be used to keep the rate of translation from DNA into protein under control. Thus identifying the promoter is essential for DNA sequence analysis. So far many methods and tools have been developed for this purpose and many have achieved high accuracy. The goal is to accuratley classify these DNA sequences with the highest achievable accuracy.

### Data:

#### Training Data

| Class of Data | Link |
| --- | --- |
| Positive (Promoter) | [Link](./data-copy/PromoterSequence.txt)
| Negative (Non-Promoter) | [Link](./data-copy/NonPromoterSequence.txt)

#### Test data
Predict the classes of the sequences given in [this](./data-copy/test.csv) csv file. The predictions should be either 0 (non-promoter) or 1 (promoter).


### Modeling:

After pre-processing the data, it was passed through several neural network architectures before the best performing architecture was identified. The highest performing model was a 1-dimensional convolutional neural network with two CNN layers followed by a bidirectional GRU layer prior to three additional internal Dense layers. Dropout layers were place between the 1st and 2nd CNN layers as well as between the GRU layer and the Dense layer.

Model train performance: 87.9%
Model test performance: 87.4%

## Conclusion
?????
