# News-Bias-Discriminator
The news bias discriminator is a Natural Language Processing (NLP) tool that is designed to classify news articles as being biased or unbiased. This tool is built using BERT and RoBERTa models, which are pre-trained deep learning models that are well-suited for NLP tasks such as text classification.

# Data

The data used to train and evaluate the tool is from the [Article-Bias-Prediction repository](https://github.com/ramybaly/Article-Bias-Prediction), which contains a large-scale dataset of 37,554 news articles from 15 major US news outlets. The articles are labeled with their bias scores based on the ratings from [AllSides](https://www.allsides.com/media-bias) and [Media Bias/Fact Check](https://mediabiasfactcheck.com/). The data is stored in individual JSON files, which are converted to a single pandas dataframe with 37,554 rows and 12 columns for easier processing and analysis.
