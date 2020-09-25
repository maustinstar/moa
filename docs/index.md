
## Predicting Mechanism of Action Based on Drug Genomics

## Summary Figure 
<a href="https://ibb.co/Xbzt8bq"><img src="https://i.ibb.co/Xbzt8bq/Screen-Shot-2020-09-24-at-5-32-40-PM.png" alt="Screen-Shot-2020-09-24-at-5-32-40-PM" align="center" border="0" width="433" height="215"/></a> 

## Introduction/Background

With the advent of more powerful technologies, drug discovery has changed from the chance-based approaches of the past to a more targeted model based on an understanding of the underlying biological mechanism of a disease. In this new framework, scientists seek to identify a protein target associated with a disease and develop a molecule that can modulate that protein target. To describe the biological activity of a given molecule, scientists assign a label referred to as mechanism-of-action (MoA). 

One approach is to treat a sample of human cells with the drug and then analyze the cellular responses with algorithms that search for similarity to known patterns in large genomic databases, such as libraries of gene expression or cell viability patterns of drugs with known MoAs. However, this method is very costly and time-consuming. 

The dataset in this project combines gene expression and cell viability data. The data is based on a new technology that measures simultaneously human cells’ responses to drugs in a pool of 100 different cell types. In addition, it has MoA annotations for more than 5,000 drugs in this dataset which will act as the targets. 

## Expected Methods

#### The Goal
Given various inputs such as gene expression and cell viability we hope to develop an algorithm that automatically labels each case in the test set as one or more MoA classes. Since drugs can have multiple MoA annotations, the task is a multi-label classification problem. 
#### Unsupervised learning 
We expect to either form clusters for each mechanism of action or we can generalize them further into classifications such as activator, inhibitor, channel blocker, etc. In terms of the specific algorithms, we plan on using K-Means and GMM. We also plan on trying PCA for dimension reduction.  
#### Supervised learning
For this part of the project we plan on using Naïve Bayes and an Artificial Neural Network. Some of the main reasons that led us to choosing these two is the high dimensionality of our data set and also our need for a probabilistic value for each classification. 
To determine our accuracy in predicting the MoA of each sig_id, we will use the following log loss equation:
<img src="https://bit.ly/3kMUv5K" align="center" border="0" alt="- \frac{1}{M} \sum_{m=1}^{M}\frac{1}{N}\sum_{i=1}^{N}[y_{i,m}log(\hat{y_{I,m}}) + (1-y_{i,m})log(1 - \hat{y_{I,m}}) ]" width="433" height="53" /> 
* N is the number of sig_id observations in the test data (i=1,…,N) 
* M is the number of scored MoA targets (m=1,…,M)
* ŷ<sub> i, m</sub>  is the predicted probability of a positive MoA response for a sig_id 
* y<sub>i, m</sub> is the ground truth, 1 for a positive response, 0 otherwise 

## Results
Based on the MoA annotations, the accuracy of solutions will be evaluated on the average value of the logarithmic loss function applied to each drug-MoA annotation pair.
If successful, we’ll develop an algorithm that can predict a compound’s MoA given its cellular signature, thus helping scientists advance the drug discovery process. 
## Discussion
We evaluate our methods based on the accuracy of solutions measured by the average value of logarithmic loss functions applied to each drug-MoA annotation pair. We compare our results to nominal values benchmarks and select the technique that produced the best overall performance. Our work could contribute to drug classification in broader scenarios and help doctors treat patients more efficiently.  
## References 
1.Peach KC, Bray WM, Winslow D, Linington PF, Linington RG. Mechanism of action-based classification of antibiotics using high-content bacterial image analysis. Mol Biosyst. 2013 Jul;9(7):1837-48. doi: 10.1039/c3mb70027e. Epub 2013 Apr 23. PMID: 23609915; PMCID: PMC3674180. 

2.Eltze M. Multiple mechanisms of action: the pharmacological profile of budipine. J Neural Transm Suppl. 1999;56:83-105. doi: 10.1007/978-3-7091-6360-3_4. PMID: 10370904. 

3.“Mechanisms of Action (MoA) Prediction.” Kaggle, www.kaggle.com/c/lish-moa/overview 

<!--
Here is a cheat sheet

# Header 1
## Header 2
### Header 3
#### Header 4

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

```
code
block
```

[Link](url) and ![Image](src)

-->
