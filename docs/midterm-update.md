# MoA Midterm Update

## Summary Figure

<img src="https://raw.githubusercontent.com/maustinstar/moa/master/docs/assets/infographic-2.png" />

## Background

Scientists seek to identify protein targets associated with a disease and then develop a molecule that can modulate that protein target. To describe the biological activity of a given molecule or drug, scientists assign a label referred to as mechanism-of-action (MoA).

The current approach to identify Moa is to treat a sample of human cells with the drug and then analyze the cellular responses with algorithms that search for similar  patterns in genomic databases, such as libraries of gene expression or cell viability patterns of drugs with known MoAs. However, this method is very costly and time-consuming.

## Dataset Information

The dataset in this project combines gene expression and cell viability data. The data is based on a new technology that measures simultaneously human cells’ responses to drugs in a pool of 100 different cell types. In addition, it has MoA annotations for more than 5,000 drugs in this dataset which will act as the targets. 

For our initial analysis, we discarded the dosage type and time because previous research studies indicate it should not significantly affect the MoAs present. Furthermore, the control vehicle is not needed because this data is already represented in the scored dataset on which our model will be trained. Finally, we normalized all gene expression values between 0 and 1.

## The Goal

Given various inputs, such as gene expression and cell viability, we hope to develop an algorithm that automatically labels each case in the test set as one or more MoA classes. Since drugs can have multiple MoA annotations, the task is a multi-label classification problem.

### Current Progress

We used PCA for dimensionality reduction. We determined that 95% is an optimal cut-off threshold and analyzed the number of components required to achieve that threshold. As shown in the figure below, the number of components needed to achieve 95% variance capture is about 525.

<img src="https://raw.githubusercontent.com/maustinstar/moa/master/docs/assets/pca-threshold.png" />

### Challenges

The main challenge we face is high dimensionality required to capture 95% of the variance in our dataset. Moreover, there are three different datasets we can use for training the model: original, PCA, or original + PCA. Performing tests to determine which dataset performs the best is necessary. Moving forward, it will be important to determine the architecture of the supervised model we will be using to perform multi-class classification.

### Next Steps

In the future, we plan on adding supervised learning techniques in addition to the PCA methods to evaluate our data set. We are considering using a Naïve Bayes and an Artificial Neural Network to find a probabilistic value for each classification. We will identify the supervised learning performance using the logarithmic loss function. We also plan on submitting our work to [Kaggle's open competition](https://maustinstar.github.io/moa/kaggle).

## Discussion

We evaluate our methods based on the accuracy of solutions measured by the average value of logarithmic loss functions applied to each drug-MoA annotation pair. We compare our results to nominal values benchmarks and select the technique that produced the best overall performance. Our work could contribute to classification of current and future drugs to help doctors discover effective treatments.

### References

1. Peach KC, Bray WM, Winslow D, Linington PF, Linington RG. Mechanism of action-based classification of antibiotics using high-content bacterial image analysis. Mol Biosyst. 2013 Jul;9(7):1837-48. doi: 10.1039/c3mb70027e. Epub 2013 Apr 23. PMID: 23609915; PMCID: PMC3674180.​

2. Eltze M. Multiple mechanisms of action: the pharmacological profile of budipine. J Neural Transm Suppl. 1999;56:83-105. doi: 10.1007/978-3-7091-6360-3_4. PMID: 10370904.

3. “Mechanisms of Action (MoA) Prediction.” Kaggle, www.kaggle.com/c/lish-moa/overview.
