# RTE-classifier
This is a research of an appropriate classifier for RTE dataset from GLUE

## Research

RTE - dataset from GLUE with two sentances for each data point to identify logics between these sentances. 

There are following aspects considered in this study:
1. **Representation function** Several assumptions are investigated based on representation of each sentences: concatenation of features of representation of two sentences might be sufficient to train classifiers how to distinguish one class from another, subtraction of features of representation might be enough of averaged addition of features of representation might be enough to train classifiers how to distinguish one class from another. The choice of these assumptions is motivated with attempt to find an optimal representation pattern which is easy to understand and not heavy to compute.
2. **Model choice.** basic classifiers and LSTM

File ```rte.ipynb``` reflects all experiments and its performance and file ```GLUE classifier.pdf``` provides with short report with analysis.

## Analysis

RTE classification is complicated with input data representation, but despite of this f1-score were achieved up
to 0.61.

1. **Sentences representation** Assumptions about the representation of two sentences resulted in weak performance of models. More advanced approaches should be applied to train a classifier.
2. **Model choice.** LSTM model was not able to correctly classify different classes. Losses values showed LSTM as overfitted from the early epochs and are only learnt to classify all instances as instances belonging to one class.
