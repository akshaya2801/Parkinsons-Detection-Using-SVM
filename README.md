# Parkinsons-Detection-Using-SVM

DATASET DESCRIPTION
Title: Oxford Parkinson's Disease Detection Dataset
-----------------------------------------------------
Data Set Characteristics: Multivariate
Number of Instances: 197
Area: Life
Attribute Characteristics: Real
Number of Attributes: 23
Date Donated: 2008-06-26
Associated Tasks: Classification
Missing Values? N/A
This dataset is composed of a range of biomedical voice measurements from 31 people, 23 with Parkinson's disease (PD). Each column in the table is a particular voice measure, and each row corresponds one of 195 voice recording from these individuals ("name" column). The main aim of the data is to discriminate healthy people from those with PD, according to "status" column which is set to 0 for healthy and 1 for PD.

Attribute Information:
Matrix column entries (attributes):
name - ASCII subject name and recording number
MDVP:Fo(Hz) - Average vocal fundamental frequency
MDVP:Fhi(Hz) - Maximum vocal fundamental frequency
MDVP:Flo(Hz) - Minimum vocal fundamental frequency
MDVP:Jitter(%),MDVP:Jitter(Abs),MDVP:RAP,MDVP:PPQ,Jitter:DDP - Several
measures of variation in fundamental frequency
MDVP:Shimmer,MDVP:Shimmer(dB),Shimmer:APQ3,Shimmer:APQ5,MDVP:APQ,Shimme
r:DDA - Several measures of variation in amplitude
NHR,HNR - Two measures of ratio of noise to tonal components in the
voice
status - Health status of the subject (one) - Parkinson's, (zero) -
healthy
RPDE,D2 - Two nonlinear dynamical complexity measures
DFA - Signal fractal scaling exponent
spread1,spread2,PPE - Three nonlinear measures of fundamental frequency variation

CONCLUSION:
Based on the results, the SVM model with RBF kernel and C=1 and 
degree=3 is the preferred choice for this classification task, as it 
achieves the highest accuracy on the test data.
Logistic Regression is also a viable option, especially considering 
its simplicity and interpretability, with similar performance to SVM 
after tuning.
KNN performs reasonably well but may require further optimization or 
feature engineering to improve its performance compared to SVM and 
Logistic Regression.
Possible Reasons why SVM outweighs KNN and Linear Regression models
1. Effective in high-dimensional spaces: SVMs perform well in highdimensional spaces, making them suitable for datasets with many features, such as the Parkinson's dataset.
2. Robust to overfitting: SVMs have a regularization parameter (C) that helps prevent overfitting by controlling the trade-off between maximizing the margin and minimizing the classification error.
3. Global optimization: SVM aims to find the hyperplane that maximizes the margin between classes, leading to better generalization to unseen data compared to local optimization approaches like KNN.
4. Kernel trick: SVMs can efficiently handle non-linear decision boundaries using the kernel trick, which transforms the input space into a higher-dimensional space, allowing it to find a linear separation.
5. Less impacted by irrelevant features: SVMs are less affected by irrelevant features compared to KNN, which relies on distance metrics and can be influenced by noisy or irrelevant features.
Overall, these factors contribute to SVM's ability to achieve higher accuracy and better generalization compared to KNN and Logistic Regression in certain scenarios, including the classification of Parkinson's disease based on the provided dataset.

REFERENCES:
Early Detection of Parkinson’s Disease using Motor symptoms and Machine Learning Poojaa C, John Sahaya Rani Alex
https://arxiv.org/ftp/arxiv/papers/2304/2304.09245.pdf
(model accuracy of 91.9%)

Tolosa, Eduardo, et al. "Challenges in the diagnosis of Parkinson's disease." The Lancet Neurology 20.5 (2021): 385-397.

Channa, Asma, Nirvana Popescu, and Vlad Ciobanu. "Wearable solutions for patients with Parkinson’s disease and neurocognitive disorder: a systematic review." Sensors 20.9 (2020): 2713.

