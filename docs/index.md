 

https://www.kaggle.com/c/lish-moa/overview 

- What are you trying to do? Articulate your objectives using absolutely no jargon. (Introduction)  

- How is it done today, and what are the limits of current practice? (Introduction)  

- What is new in your approach and why do you think it will be successful? (Methods)  

- Who cares? If you are successful, what difference will it make? (Discussion)  

- What are the risks? (Methods)  

- How much will it cost? (Methods)  

- How long will it take? (Methods)  

- What are the mid-term and final “exams” to check for success? (Results)

## Summary Figure 

## Introduction/Background
#### Suraj 

With the advent of more powerful technologies, drug discovery has changed from the chance-based approaches of the past to a more targeted model based on an understanding of the underlying biological mechanism of a disease. In this new framework, scientists seek to identify a protein target associated with a disease and develop a molecule that can modulate that protein target. To describe the biological activity of a given molecule, scientists assign a label referred to as mechanism-of-action (MoA). 

One approach is to treat a sample of human cells with the drug and then analyze the cellular responses with algorithms that search for similarity to known patterns in large genomic databases, such as libraries of gene expression or cell viability patterns of drugs with known MoAs. However, this method is very costly and time-consuming. 

The dataset in this project combines gene expression and cell viability data. The data is based on a new technology that measures simultaneously human cells’ responses to drugs in a pool of 100 different cell types. In addition, it has MoA annotations for more than 5,000 drugs in this dataset which will act as the targets. 

This project will look to develop an algorithm that automatically labels each case in the test set as one or more MoA classes. Since drugs can have multiple MoA annotations, the task is a multi-label classification problem. 

## Expected Methods
#### Prathic 

Unsupervised learning – clustering mechanism based on specific mechanism (206 clusters) or more general subcategories (inhibitor, agonist, etc.) 

Supervised learning - some sort of predictive classification  

## Results
#### John 

Based on the MoA annotations, the accuracy of solutions will be evaluated on the average value of the logarithmic loss function applied to each drug-MoA annotation pair. 

If successful, you’ll help to develop an algorithm to predict a compound’s MoA given its cellular signature, thus helping scientists advance the drug discovery process. 

## Discussion
#### John 

## References 


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
