# Toxic Comment Classification Challenge

This repo contains the code that I wrote for Kaggle NLP challenge - [Toxic Comment Classification](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge)

## About the challenge (from Kaggle)
In this competition, you’re challenged to build a multi-headed model that’s capable of detecting different types of of toxicity like threats, obscenity, insults, and identity-based hate better than Perspective’s current models. You’ll be using a dataset of comments from Wikipedia’s talk page edits. Improvements to the current model will hopefully help online discussion become more productive and respectful.

## Tools required
1. _Python 3.5+_
2. _NLTK_
3. _Numpy_
4. _Pandas_
5. _Sklearn_
5. _Keras_
6. _Tensorflow_
7. _Glove word embedding_
8. _Fasttext word embedding_

## How to run
Model needs to be set in the fit_predict.py. The code trains the model with k fold cross validation. It save the trained model and predictions.
   
`python fit_predict.py train_data_path test_data_path pretrained_embedding_path --result-path  --sentences-length --fold-count --dense-size --modelname-prefix --batch-size --dropout-rate`

#### Sample execution command
`python fit_predict.py ./data/train.csv ./data/test.csv ./NLP/fasttext_embedding/crawl-300d-2M.vec --result-path ./toxic_results --sentences-length 400 --fold-count 10 --dense-size 256 --modelname-prefix dpcnn400_fasttextcrawl --batch-size 512 --dropout-rate 0.4`
