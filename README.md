# News-Bias-Discriminator
The news bias discriminator is a Natural Language Processing (NLP) tool that is designed to classify news articles as being biased or unbiased.I will fine tune different LLMs, to see which performs the best.

# Data

The data used to train and evaluate the tool is from the [Article-Bias-Prediction repository](https://github.com/ramybaly/Article-Bias-Prediction), which contains a large-scale dataset of 37,554 news articles from 15 major US news outlets. The articles are labeled with their bias scores based on the ratings from [AllSides](https://www.allsides.com/media-bias) and [Media Bias/Fact Check](https://mediabiasfactcheck.com/). The data is stored in individual JSON files, which are converted to a single pandas dataframe with 37,554 rows and 12 columns for easier processing and analysis.


# Models

## DistillBERT

I fine-tuned a DistilBERT uncased model on a dataset of nearly 12,000 data points to reduce the training time. The test set comprised 20% of the total dataset. The evaluation loss was approximately 0.10, which is a promising result.


## Roberta

- Accuracy: 81%
- Eval loss: 0.5
-  MAE: 0.25


