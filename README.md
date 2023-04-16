# News-Bias-Discriminator
The news bias discriminator is a Natural Language Processing (NLP) tool that is designed to classify news articles as being biased or unbiased.The basic idea is to fine-tune some large language models like BERT, ROBERTA and DISTILBERT, and see which one performs the best.

# Data

The data used to train and evaluate the tool is from the [Article-Bias-Prediction repository](https://github.com/ramybaly/Article-Bias-Prediction), which contains a large-scale dataset of 37,554 news articles from 15 major US news outlets. The articles are labeled with their bias scores based on the ratings from [AllSides](https://www.allsides.com/media-bias) and [Media Bias/Fact Check](https://mediabiasfactcheck.com/). The data is stored in individual JSON files, which are converted to a single pandas dataframe with 37,554 rows and 12 columns for easier processing and analysis.

# Training

In the "models" folder, I trained some models (BERT, ROBERTA, DISTILBERT), on a smaple dataset of 6000 - 12000 news articles to see the intial results of how the models performed on the dataset, based on the testing, I found BERT to be the most suitable.

In the "MODELS_MAIN" folder, I trained BERT on 50% and 100% of the news articles of the dataset, of which are the following results:

## On 50% of the dataset
- Val Accuracy: 74%
- F1 score (macro): 0.75
- Class imbalance score: 0.75
- Here is the confusion matrix of the model:

![download (1)](https://user-images.githubusercontent.com/91069648/232327046-c1934e0a-64cf-405f-80f8-cdd7c451687f.png)



## On 100% of the dataset
- Val Accuracy: 78%
- F1 score (macro): 0.77
- Class imbalance score:  0.78
- Here is the confusion matrix of the model:

![download (2)](https://user-images.githubusercontent.com/91069648/232327155-7ba4416b-667d-4476-9b06-652b300e4796.png)


## Note: 
As BERT model has a maximum sequence length of 512 tokens, and the news articles on the dataset had sequence length in the range of 1200 - 10000 tokens, so I used the window sliding method by splitting the long articles into smaller sections and feeding them to the model separately.

