# Kaggle Competition

> The original competition is hosted on [Kaggle](https://www.kaggle.com/c/lish-moa/overview).
>
> This page contains a copy of the project details.

## Mechanisms of Action (MoA) Prediction
### Can you improve the algorithm that classifies drugs based on their biological activity?
#### Laboratory for Innovation Science at Harvard

## Overview

### Description

The [Connectivity Map](https://clue.io/), a project within the Broad Institute of MIT and Harvard, together with the [Laboratory for Innovation Science at Harvard (LISH)](http://lish.harvard.edu/), presents this challenge with the goal of advancing drug development through improvements to MoA prediction algorithms.

#### What is the Mechanism of Action (MoA) of a drug? And why is it important?

In the past, scientists derived drugs from natural products or were inspired by traditional remedies. Very common drugs, such as paracetamol, known in the US as acetaminophen, were put into clinical use decades before the biological mechanisms driving their pharmacological activities were understood. Today, with the advent of more powerful technologies, drug discovery has changed from the serendipitous approaches of the past to a more targeted model based on an understanding of the underlying biological mechanism of a disease. In this new framework, scientists seek to identify a protein target associated with a disease and develop a molecule that can modulate that protein target. As a shorthand to describe the biological activity of a given molecule, scientists assign a label referred to as mechanism-of-action or MoA for short.

#### How do we determine the MoAs of a new drug?

One approach is to treat a sample of human cells with the drug and then analyze the cellular responses with algorithms that search for similarity to known patterns in large genomic databases, such as libraries of gene expression or cell viability patterns of drugs with known MoAs.

In this competition, you will have access to a unique dataset that combines gene expression and cell viability data. The data is based on a new technology that measures simultaneously (within the same samples) human cells’ responses to drugs in a pool of 100 different cell types (thus solving the problem of identifying ex-ante, which cell types are better suited for a given drug). In addition, you will have access to MoA annotations for more than 5,000 drugs in this dataset.

As is customary, the dataset has been split into testing and training subsets. Hence, your task is to use the training dataset to develop an algorithm that automatically labels each case in the test set as one or more MoA classes. Note that since drugs can have multiple MoA annotations, the task is formally a multi-label classification problem.

#### How to evaluate the accuracy of a solution?

Based on the MoA annotations, the accuracy of solutions will be evaluated on the average value of the [logarithmic loss function](https://www.kaggle.com/c/lish-moa/overview/evaluation) applied to each drug-MoA annotation pair.

If successful, you’ll help to develop an algorithm to predict a compound’s MoA given its cellular signature, thus helping scientists advance the drug discovery process.

### Evaluation

> Honestly, this section has so many notation formatting, it's easier to drop the link.

[https://www.kaggle.com/c/lish-moa/overview/evaluation](https://www.kaggle.com/c/lish-moa/overview/evaluation)

### Timeline

- November 23, 2020 - Entry deadline. You must accept the competition rules before this date in order to compete.
- November 23, 2020 - Team Merger deadline. This is the last day participants may join or merge teams.
- November 30, 2020 - Final submission deadline.

All deadlines are at 11:59 PM UTC on the corresponding day unless otherwise noted. The competition organizers reserve the right to update the contest timeline if they deem it necessary.

### Prizes

- 1st Place - $12,000
- 2nd Place - $8,000
- 3rd Place - $5,000
- 4th Place - $5,000

To ensure reproducibility of the top solutions, all winners must provide their code and documentation necessary to train and test their algorithms on the same data. To avoid dependency problems, competitors are strongly encouraged to share their code in a Docker container or via an equivalent method.

All teams, regardless of place, are also strongly encouraged and invited to share a written description of their solution (and open source their code, if willing). Your contributions will help scientists advance the drug discovery process.

### Code Requirements

Submissions to this competition must be made through Notebooks. In order for the "Submit to Competition" button to be active after a commit, the following conditions must be met:

- CPU Notebook <= 9 hours run-time
- GPU Notebook <= 2 hours run-time
- No internet access enabled
- Freely & publicly available external data is allowed, including pre-trained models
- Submission file must be named submission.csv

Please see the [Code Competition FAQ](https://www.kaggle.com/docs/competitions#kernels-only-FAQ) for more information on how to submit.

### Useful Links

[Connectopedia](https://clue.io/connectopedia/glossary) is a free, web-based dictionary of terms and concepts related to the Connectivity Map (including definitions of cell viability and gene expression data in that context)

#### Related papers

- Corsello et al. “Discovering the anticancer potential of non-oncology drugs by systematic viability profiling,” Nature Cancer, 2020, [https://doi.org/10.1038/s43018-019-0018-6](https://doi.org/10.1038/s43018-019-0018-6)
- Subramanian et al. “A Next Generation Connectivity Map: L1000 Platform and the First 1,000,000 Profiles,” Cell, 2017, [https://doi.org/10.1016/j.cell.2017.10.049](https://doi.org/10.1016/j.cell.2017.10.049)
