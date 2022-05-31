# My_projects
Building_AI_course_idea
<!-- This is the markdown template for the final project of the Building AI course, 
created by Reaktor Innovations and University of Helsinki. 
Copy the template, paste it to your GitHub README and edit! -->

# Project Title
A human in the loop labelling of text datasets for emotion detection in customer online reviews.

## Summary
This projects aims at labelling text data sets using existing NLP tools for emotion detection and a small sample mannually annotated.

## Background

I am interested in assesing emotions in customer online reviews of products and services. I have used different open codes and tools for that, bur results have not been satisfactory:
.- They use different sets of emotions (Nrclex issues the probability of a text associate each of the 8 basic emotions from Plutchik (1980): anger, fear, anticipation, trust, surprise, sadness, joy and disgust, as well as sentiment either positive and negative) whereas different ML models use a texts dataset annotated in 6 categories from Ekman model (joy, sadness, fear, surprise, anger and love, https://www.kaggle.com/rizkyalifr/emotions-recognition-from-text-with-linearsvc; https://www.kaggle.com/datasets/ishantjuyal/emotions-in-text?resource=download)
.- Also, none of them apply emotions which could be expected for products and services such as boring, relax, or indifference
.- NRClex did not assigned any emotion to a high percentage (more than 45%) of online comments for some products and services, whereas it was only 9,9% for a dataset with 18000 texts from books.
.- Results from Nrclex and ML models for online comments and for book texts were quite different in emotions distribution and probabilities. ML models issued better results, but have only 6 emotional labels.
It seems that results depend much on the dataset or lexicon used for developing the model, that is on the people that annotated them. A specific dataset seems necessary for developing a ML model for detecting emotions in customer online reviews.
Labelling datasets for supervised ML is a bottleneck in many AI projects. As an alternative, automatic and programmatic labelling tools are being developed. These approaches, in a few words, use human annotators to label a random percentage of the dataset which is used to develop a first classifier and confidence metrics and thresholds for the labels. The model is used to label the rest of the dataset and the metrics to compute the quality of the labelling in a series of loops till desired quality is reached. As far as I know, this is avaiable for image datasets, texts classification and others but not for emotions detection in texts.
My idea is to use the existing codes for automatic emotions labelling of specific datasets.

## Data sources and AI methods

The main data source is my own dataset (df) with on-line comments for different products and services. I will mannually annotate 10-20% of comments (df1). 
Then I will develop a ML classifier (model 1) with df1, having df1 for train and df1 for test the model performance (P1). I would need applying NLP for text mining and pre-processing.
I would apply model 1, NRClex and an existing ML model (https://www.kaggle.com/rizkyalifr/emotions-recognition-from-text-with-linearsvc; https://www.kaggle.com/datasets/ishantjuyal/emotions-in-text?resource=download) for labelling the rest of comments (df –df1= dft) and assign an average probability for each comment and label for each comment. This way, the seed label will “summarize” the perception of three “teams” of labellers.
A second ML model (model 2) will be developed with this dataset and performance asessed against df1test (P2).
Then, an iterative process will be done till performance reaches a given threshold. 
In the process, probabilities in dft will be modified according to differences between predicted and true probabilities, as well as according to differences in emotions distribution between df1 and dft.

## How is it used?

The solution will be used:
Annotated dataset: for people interested in studying emotions in customer onlien reviews of products and services with different purposes, for example to stablish the influence of emotions in general stars ranking.
The Ai solution: for annotating other datasets for other domains.

## Challenges

The Project has clear mathematical and statistical weaknesses, also automation of the process is to be solved

## What next?
As the code will be used, more and more annotated texts will be available and the process will improve. But, it couls grow to be applied as a general purpose autolabelling tool.

## Acknowledgments
I would apply model 1, NRClex and an existing dataset and ML model from (https://www.kaggle.com/rizkyalifr/emotions-recognition-from-text-with-linearsvc; https://www.kaggle.com/datasets/ishantjuyal/emotions-in-text?resource=download) 
